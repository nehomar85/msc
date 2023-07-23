function formatnum(fstr){
	var fnum = "";
	var pun = -10;
	var pos = true;
	if(isNaN(fstr) == true)
		return fstr;
	fstr = parseFloat(fstr).toString();
	if (fstr<0)
	{
		fstr = (fstr * -1)+"";
		pos = false;
	}
	for(i=0; i<fstr.length; i++)
		if (fstr.charAt(i) == ".")
		{
			fnum = fstr.substring(i,fstr.length);
			pun = i-1;
		}
	if(pun == -10)
		pun = fstr.length - 1;
	for(; pun>=3; pun-=3)
		fnum = "," + fstr.substring(pun - 2,pun+1)+ fnum;
	pun += 1;
	if((fnum.length < 3)&&(fnum.length > 0))
	    fnum = fnum + "0";
	if(fnum.length == 0)
	    fnum = fnum + ".00";
	fnum = fstr.substring(0,pun) + fnum;
	if (!pos)
		fnum = "-" + fnum;
	return fnum;
}
function openlov(pagina) { 
	var lTop=screen.availHeight, lLeft=screen.availWidth;
	var w = window.open(pagina, "LOV" + pagina.substring(0,15).replace(".",""), "Scrollbars=1, resizable=1, width=" + lLeft + ", height=" + lTop + ", top=0, left=0");
} 
function Ubicar() 
{ 
	document.body.onbeforeprint = BeforePrint;
	document.body.onafterprint = AfterPrint;
	for(var i=0; i<document.forms[0].elements.length; i++)
		if(document.forms[0].elements[i].readOnly == false && document.forms[0].elements[i].disabled == false && document.forms[0].elements[i].type != "hidden")
		{ 
			document.forms[0].elements[i].focus(); 
			if(document.forms[0].elements[i].select) 
			document.forms[0].elements[i].select(); 
			return; 
		} 
} 
function esconder() 
{ 
	if(document.F.salv) 
		document.F.salv.style.display = "none"; 
	if(document.F.cons) 
		document.F.cons.style.display = "none"; 
	if(document.F.inse) 
		document.F.inse.style.display = "none"; 
	if(document.F.elim) 
		document.F.elim.style.display = "none"; 
	if(document.F.canc) 
		document.F.canc.style.display = "none"; 
	if(document.F.prev) 
		document.F.prev.style.display = "none"; 
} 
function mostrar() 
{ 
	if(document.F.salv) 
		document.F.salv.style.display = ""; 
	if(document.F.cons) 
		document.F.cons.style.display = ""; 
	if(document.F.inse) 
		document.F.inse.style.display = ""; 
	if(document.F.elim) 
		document.F.elim.style.display = ""; 
	if(document.F.canc) 
		document.F.canc.style.display = ""; 
	if(document.F.prev) 
		document.F.prev.style.display = ""; 
} 
function desformatnum(fstring) 
{ 
	var fnum = ""; 
	var i=0; 
	for(i=0; i<fstring.length; i++) 
		if(fstring.charAt(i) != sepmiles && fstring.charAt(i) != " ") 
			fnum = fnum + fstring.charAt(i); 
	if(isNaN(parseFloat(fnum))) 
		fnum = ""; 
	return fnum; 
} 
function desblancos(fstring) 
{ 
	var fnum = ""; 
	var i=0; 
	var letra = "N"; 
	for(i=0; i<fstring.length; i++) 
		if((fstring.charAt(i) != " " || letra == "S") && fstring.charAt(i) != '"' && fstring.charAt(i) != "'") 
		{ 
			letra = "S"; 
			fnum = fnum + fstring.charAt(i); 
		} 
	for(i=fnum.length-1; i>=0; i--) 
		if(fnum.charAt(i) == " ") 
			fnum = fnum.substring(0,i); 
		else 
			break; 
	return fnum; 
} 
function salto() 
{ 
	event.cancelBubble = true; 
	if(event.keyCode==13) 
		event.keyCode=9; 
	if(event.keyCode==9) 
	{ 
	 for(var i=0; i<document.forms[0].all.length; i++) 
	 { 
		if(document.forms[0].all[i] == event.srcElement) 
		{ 
			if(event.shiftKey && event.keyCode==9) 
			{ 
				for(var j=i-1; j>=0; j--) 
				{ 
					if(!document.forms[0].all[j].disabled && !document.forms[0].all[j].readOnly 
						&& document.forms[0].all[j].style.display == "" && document.forms[0].all[j].type) 
					{ 
						var visible = true; 
						var p1 = document.forms[0].all[j].parentNode; 
						while(p1) 
						{ 
							if(p1.style) 
								if (p1.style.display == "none") 
									visible = false; 
							p1 = p1.parentNode; 
						} 
						if(document.forms[0].all[j].type!="hidden" && visible) 
						{ 
						    if(document.forms[0].all[j].name!="PVALOR_PAGADO"){
							    document.forms[0].all[j].focus(); 
								if(document.forms[0].all[j].select) 
							    document.forms[0].all[j].select(); 
							    event.returnValue = false; 
							    return; 
							}
							return; 
						} 
					} 
					if(j==0) 
						j=document.forms[0].all.length; 
				} 
			} 
			if(!event.shiftKey && event.keyCode==9) 
			{ 
				for(var j=i+1; j<document.forms[0].all.length; j++) 
				{ 
					if(!document.forms[0].all[j].disabled && !document.forms[0].all[j].readOnly 
						&& document.forms[0].all[j].style.display != "none" && document.forms[0].all[j].type) 
					{ 
						var visible = true; 
						var p1 = document.forms[0].all[j].parentNode; 
						while(p1) 
						{ 
							if(p1.style) 
								if (p1.style.display == "none") 
									visible = false; 
							p1 = p1.parentNode; 
						} 
						if(document.forms[0].all[j].type!="hidden" && visible) 
						{ 
						    if(document.forms[0].all[j].name!="PVALOR_PAGADO"){
							    document.forms[0].all[j].focus(); 
							    if(document.forms[0].all[j].select) 
							    document.forms[0].all[j].select(); 
							    event.returnValue = false; 
							    return; 
							}
							return; 
						} 
					} 
					if(j==document.forms[0].all.length-1) 
						j=-1; 
				} 
			} 
		} 
	 } 
	} 
} 
function mousemove() 
{
	if(CMenu>0 && FocMenu==0)
		HideM();
}
function imprimir()
{
	BeforePrint();
	window.print();
	AfterPrint();
} 
function show_help()
{
var HPage = document.F.action; 
pos = HPage.lastIndexOf("?"); if(pos>0) HPage = HPage.substr(0,pos); 
pos = HPage.lastIndexOf("/"); HPage = HPage.substr(pos+1); 
pos = HPage.lastIndexOf("."); Page = HPage.substr(pos+1); 
HPage = HPage.substr(0,pos) + ".mostrar_ayuda?ppagina=" + Page; 
	var nWin=window.open(HPage, "help");
}
function MoveMenu()
{
	if(document.getElementById("MenuPane"))
		document.getElementById("MenuPane").style.top = document.body.scrollTop + 10;
}
function validar(Objeto, Titulo, TipoDato, Decimales, Obliga, Ver, ValorMinimo, ValorMaximo)
{
	var Valor = desblancos(Objeto.value);
	Objeto.value = Valor;
	if(Obliga=="OBL")
	{
		if (Valor.length < 1)
		{
            alert("El campo " + Titulo + " es obligatorio.");
            if(Ver!="OCULTO")
                if(Objeto.getAttribute("TYPE")!="hidden")
				         if(Objeto.focus()!=null){
				             Objeto.focus();
				             Objeto.select();
				         }
            return false;
        }
	}
	if(TipoDato=="ENT"||TipoDato=="FLT")
	{
		if (Valor.length > 0)
		{
			Valor = desformatnum(Valor)
			if (isNaN(parseFloat(Valor,10)))
			{
			    alert("El campo " + Titulo + "( " + Valor + " ) debe ser numerico.");
			    if(Ver!="OCULTO") {
					Objeto.focus();
				    Objeto.select(); } 
			    return false;
			}
			if (parseFloat(Valor,10) < ValorMinimo)
			{
			    alert("El campo " + Titulo + "( " + Valor + " ) debe ser mayor o igual a " + ValorMinimo.toString());
			    if(Ver!="OCULTO") { 
					Objeto.focus();
				    Objeto.select(); }
			    return false;
			}
			if (parseFloat(Valor,10) > ValorMaximo)
			{
			    alert("El campo " + Titulo + "( " + Valor + " ) debe ser menor o igual a " + ValorMaximo.toString());
			    if(Ver!="OCULTO"){
					Objeto.focus();
				    Objeto.select(); }
			    return false;
			}
			var intPos = Valor.indexOf(".");
			if(TipoDato=="FLT")
			{
				if(intPos > 0)
				{
					if(Decimales > 0)
					{
						Objeto.value = Valor.substring(intPos + 1, Valor.length);
						if(!validar(Objeto, "number of decimals of " + Titulo, "ENT", 0, "OBL", Ver, 0, Math.pow(10, Decimales) - 1))
						{
							Objeto.value = Valor;
							return false;
						}
						Objeto.value = Valor;
					}
					else
					{
						if(intPos > 0)
						{
							alert("El campo " + Titulo + " no debe tener decimales ");
							if(Ver!="OCULTO") {
								Objeto.focus();
				             	Objeto.select(); }
							return false;
						}
					}
				}
			}
			else
			{
				if(intPos > 0)
				{
					alert("El campo " + Titulo + " no debe tener decimales ");
					if(Ver!="OCULTO") { 
						Objeto.focus();
				        Objeto.select(); }
					return false;
				}
			}
		}
	}
	if(TipoDato=="FCH")
	{
		if (Valor.length > 0)
		{
	        if (!jesfecha(Valor))
			{
        	    alert("El campo " + Titulo + " debe ser una fecha valida (" + formatofecha + ") ");
	            if(Ver!="OCULTO") { 
					Objeto.focus();
				    Objeto.select(); } 
				return false;
			}
		}
	}
	return true;
}
function validarTecla(event,li_tipo)
{
	var li_kc=event.keyCode;
	switch(li_tipo)
	{
		case "AL":
			if(li_kc==39||li_kc==34)
				event.returnValue=false;
			break;
		case "FE":
			if(li_kc<47||li_kc>57)
				event.returnValue=false;
			break;
		case "EN":
			if(li_kc<48||li_kc>57)
				event.returnValue=false;
			break;
		case "DE":
			if(li_kc!=46 && (li_kc<48||li_kc>57))
				event.returnValue=false;
			break;
		case "NO":
			if((li_kc<97||li_kc>122)&&(li_kc<65||li_kc>90)&&(li_kc<48||li_kc>57))
				event.returnValue=false;
			break;
	}
}
function jesfecha(fstring, anoini, anofin) 
{ 
	var ano;
	var mes;
	var dia;
	if(formatofecha == "DD/MM/YYYY") {
		ano = parseInt(fstring.substring(6,10),10); 
		mes = parseInt(fstring.substring(3,5),10); 
		dia = parseInt(fstring.substring(0,2),10); } 
	else {
		ano = parseInt(fstring.substring(6,10),10); 
		dia = parseInt(fstring.substring(3,5),10); 
		mes = parseInt(fstring.substring(0,2),10); } 
	var vanoini=1870; 
	var vanofin=2020; 
	if(isNaN(parseInt(anoini,10)) == false) 
		vanoini = parseInt(anoini,10); 
	if(isNaN(parseInt(anofin,10)) == false) 
		vanofin = parseInt(anofin,10); 
	if(fstring.length != 10) 
	{ 
		alert("La fecha "+fstring+" debe estar en formato " + formatofecha); 
		return false; 
	} 
	if(isNaN(dia) == true) 
	{ 
		alert("El dia "+fstring.substring(0,2)+" no es un numero."); 
		return false; 
	} 
	if(isNaN(mes) == true) 
	{ 
		alert("El mes "+fstring.substring(3,5)+" no es un numero."); 
		return false; 
	} 
	if(isNaN(ano) == true) 
	{ 
		alert("El a?o "+fstring.substring(6,10)+" no es un numero."); 
		return false; 
	} 
	if(ano<vanoini) 
	{ 
		alert("El a?o debe estar entre " + vanoini + " y " + vanofin + " y el a?o digitado es " + ano); 
		return false; 
	} 
	if(ano>vanofin) 
	{ 
		alert("El a?o debe estar entre " + vanoini + " y " + vanofin + " y el a?o digitado es " + ano); 
		return false; 
	} 
	if((mes<1) || (mes>12)) 
	{ 
		alert("El mes " + mes + " es invalido."); 
		return false; 
	} 
	if((dia<1) || (dia>31)) 
	{ 
		alert("El dia " + dia + " es invalido."); 
		return false; 
	} 
	if(((mes==2) || (mes==4) || (mes==6) || (mes==9) || (mes==11)) && (dia==31)) 
	{ 
		alert("El dia " + dia + " es invalido para el mes digitado."); 
		return false; 
	} 
	if(dia<29) 
		return true; 
	if(mes!=2) 
		return true; 
	var bisiesto = (Math.floor(ano/4) * 4 ) - ano; 
	if((bisiesto==0) && (dia>29)) 
	{ 
		alert("El dia " + dia + " es invalido para el mes digitado."); 
		return false; 
	} 
	if((bisiesto!=0) && (dia>28)) 
	{ 
		alert("El dia " + dia + " es invalido para el mes digitado."); 
		return false; 
	} 
	return true; 
} 
function FechaMenor(dtFechaIni, dtFechaFin, Titulo) 
{ 
		var valFechaIni, valFechaFin; 
		valFechaIni = parseInt(dtFechaIni.substring(6,10),10) * 365; 
		valFechaIni = valFechaIni + parseInt(dtFechaIni.substring(3,5),10) * 30; 
		valFechaIni = valFechaIni + parseInt(dtFechaIni.substring(0,2),10); 
		valFechaFin = parseInt(dtFechaFin.substring(6,10),10) * 365; 
		valFechaFin = valFechaFin + parseInt(dtFechaFin.substring(3,5),10) * 30; 
		valFechaFin = valFechaFin + parseInt(dtFechaFin.substring(0,2),10); 
		if(valFechaFin>valFechaIni) 
		{ 
			return false; 
		} 
		return true; 
} 
