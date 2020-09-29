# Image-Picker
Una Libreria De Image Picker Basada En Mediastore Con La Inspiracion Del ImagePicker De Instagram Y Creada En AIDE

Su Uso Es Muy Simple Solo Basta Con Pocas Lineas De Código
PickerBuilder builder = new PickerBuilder();
builder.init(contexto);
Para Mostrarlo Solo Utize
PickerBuilder builder= new PickerBuilder();
builder.init(contexto).show();
Para Tener Control Sobre Los Button
	final PickerBuilder builder = new PickerBuilder();
		builder.init(getActivity()).setPositiveButton("Seleccionar", new PickerOnClickListener(){

				@Override
				public void onClick(Picker picker)
				{
					picker.exit();
				}
			}).setExitPicker(new PickerOnClickListener(){

				@Override
				public void onClick(Picker picker)
				{
					picker.exit();
				}

					
				}).show();
Para Devolver La Ruta Del Archivo Seleccionado Solo Utilize
	final PickerBuilder builder = new PickerBuilder();
		builder.init(getActivity()).setPositiveButton("Seleccionar", new PickerOnClickListener(){

				@Override
				public void onClick(Picker picker)
				{
					String path = builder.getFullPath();
					Toast.makeText(getContext(),"Ruta: " + path,Toast.LENGTH_LONG).show();
					picker.exit();
				}
			}).setExitPicker(new PickerOnClickListener(){

				@Override
				public void onClick(Picker picker)
				{
					picker.exit();
				}

					
				}).show();
Tenga En Cuenta Que La Ruta Se Devuelve En Un String
