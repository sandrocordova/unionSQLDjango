# unionSQLDjango
hacer union de dos tablas en SQL  DJango


#post2 =  Direccion.objects.using('clientes').filter(CLIE_CODIGO=clienteId).values_list("DIRE_DESCRIPCION").union(TipoDireccion.objects.using('clientes').all().values_list("TIDE_DESCRIPCION"))
        #post2 =  Direccion.objects.using('clientes').filter(CLIE_CODIGO=clienteId).filter(DIRE_DESCRIPCION=TipoDireccion.objects.using('clientes').all().values_list("TIDE_DESCRIPCION"))
        #post2 =  Direccion.objects.using('clientes').filter(CLIE_CODIGO=clienteId).annotate(ejemplo = TipoDireccion.objects.using('clientes').all().values_list("TIDE_DESCRIPCION"))
        #print(post2)
