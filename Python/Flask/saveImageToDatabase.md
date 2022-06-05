一、需求提出

在一个以flask为框架的项目中，有时需要把上传的图片存入数据库以保障不易丢失。

二、原理

以二进制流的形式把上传的图片存入数据库

三、实践

(1)app/models.py中的主要代码如下：

class ImageFile(db.Model):

__tablename__ = 'ImageFile'

id = db.Column(db.Integer, primary_key=True)

image_name = db.Column(db.String(30), index=True)

image = db.Column(db.LargeBinary(length=2048))

其中存储图片时用到的字段类型为 db.LargeBinary ，这个类型就是用来储存二进制文件的。

(2)app/main/forms.py表单类的代码如下：

from flask_wtf import Form

from wtforms import StringField, FileField, SubmitField

class upForm(Form):

name = StringField('Name')

file = FileField('file')

submit = SubmitField('submit')

(3)app/main/views.py视图函数主要代码如下：

import base64

@main.route('/', methods=['GET', 'POST'])

def upload():

ds = ImageFile.query.all()

form = upForm()

if request.method == 'POST' and form.validate():

file = request.files['file'].read()

file_name = form.name.data

image_file = ImageFile(image_name=file_name, image=file)

db.session.add(image_file)

db.session.commit()

flash('ok')

return redirect(url_for('.upload'))

return render_template('up.html', form=form, ds=ds, base64=base64)

其中用request.files['file']的read()方法把图片数据读出来，然后进行数据库的储存。在显示时要用到base64这个库

(4)templates/up.html的模板文件中的主要代码如下：

{% extends "base.html" %}

{% block page_content %}

{{form.hidden_tag()}}

{{ form.name }}

{{ form.file(required="required") }}

{{ form.submit }}

----------------------------------------------------------------------------------

{% if ds %}

{% for d in ds%}

{{ d.image_name }}---

{% endfor %}

{% endif %}

{% endblock %}

在form表单元素中不要忘记加了enctype="multipart/form-data"这个属性。他能保证文件的完整传输。
