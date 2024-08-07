# TFM-drugsGenerative

Descripción detallada de cada uno de los atributos del JSON, que representa datos de etiquetas de medicamentos de OpenFDA:

### Atributos del JSON

#### Meta
- **meta.disclaimer**: Aviso legal que indica que no se debe confiar en OpenFDA para tomar decisiones médicas y que los datos pueden no estar validados.
- **meta.terms**: Enlace a los términos de servicio de OpenFDA.
- **meta.license**: Enlace a la licencia bajo la cual se proporcionan los datos.
- **meta.last_updated**: Fecha de la última actualización de los datos.
- **meta.results.skip**: Número de registros omitidos en la consulta.
- **meta.results.limit**: Límite de registros devueltos por la consulta.
- **meta.results.total**: Número total de registros disponibles.

#### Results
Esta sección contiene una lista de objetos, cada uno representando una etiqueta de medicamento con múltiples atributos. A continuación se describen estos atributos:

- **spl_product_data_elements**: Elementos de datos del producto según la etiqueta del medicamento.
- **spl_unclassified_section**: Sección de la etiqueta no clasificada en otras categorías.
- **boxed_warning**: Advertencias enmarcadas, que son alertas críticas sobre los riesgos asociados con el uso del medicamento.
- **description**: Descripción del medicamento, sus componentes y su propósito.
- **clinical_pharmacology**: Información sobre la farmacología clínica del medicamento, incluyendo su acción y efectos en el cuerpo.
- **clinical_pharmacology_table**: Tablas relacionadas con la farmacología clínica.
- **microbiology**: Información microbiológica relevante para el medicamento.
- **indications_and_usage**: Indicaciones y uso del medicamento, describiendo para qué condiciones es adecuado.
- **contraindications**: Contraindicaciones, es decir, situaciones en las que no se debe usar el medicamento.
- **warnings**: Advertencias sobre el uso del medicamento, incluyendo posibles efectos adversos.
- **precautions**: Precauciones que deben tomarse al usar el medicamento.
- **general_precautions**: Precauciones generales adicionales.
- **information_for_patients**: Información que debe ser proporcionada a los pacientes sobre el uso del medicamento.
- **laboratory_tests**: Pruebas de laboratorio recomendadas o requeridas mientras se usa el medicamento.
- **drug_interactions**: Interacciones del medicamento con otros fármacos.
- **drug_and_or_laboratory_test_interactions**: Interacciones del medicamento con pruebas de laboratorio.
- **carcinogenesis_and_mutagenesis_and_impairment_of_fertility**: Información sobre el potencial del medicamento para causar cáncer, mutaciones o afectar la fertilidad.
- **pregnancy**: Información sobre el uso del medicamento durante el embarazo.
- **labor_and_delivery**: Información sobre el uso del medicamento durante el trabajo de parto y el parto.
- **nursing_mothers**: Información sobre el uso del medicamento en madres lactantes.
- **pediatric_use**: Información sobre el uso del medicamento en pacientes pediátricos.
- **geriatric_use**: Información sobre el uso del medicamento en pacientes geriátricos.
- **adverse_reactions**: Reacciones adversas reportadas asociadas con el uso del medicamento.
- **drug_abuse_and_dependence**: Información sobre el potencial de abuso y dependencia del medicamento.
- **controlled_substance**: Clasificación del medicamento como sustancia controlada.
- **abuse**: Información adicional sobre el abuso del medicamento.
- **dependence**: Información adicional sobre la dependencia del medicamento.
- **overdosage**: Información sobre los efectos y el manejo de una sobredosis del medicamento.
- **clinical_studies**: Resúmenes de estudios clínicos realizados con el medicamento.
- **clinical_studies_table**: Tablas relacionadas con los estudios clínicos.
- **dosage_and_administration**: Información sobre la dosificación y administración del medicamento.
- **dosage_and_administration_table**: Tablas relacionadas con la dosificación y administración.
- **how_supplied**: Información sobre cómo se suministra el medicamento.
- **how_supplied_table**: Tablas relacionadas con el suministro del medicamento.
- **storage_and_handling**: Información sobre el almacenamiento y manejo del medicamento.
- **spl_medguide**: Guía de medicación para el paciente.
- **spl_medguide_table**: Tablas relacionadas con la guía de medicación.
- **package_label_principal_display_panel**: Información del panel principal de la etiqueta del paquete.
- **set_id**: Identificador del conjunto de datos.
- **id**: Identificador único del medicamento.
- **effective_time**: Fecha de efectividad de la información del medicamento.
- **version**: Versión de la información del medicamento.

#### OpenFDA
Esta sección contiene información adicional proporcionada por OpenFDA.

- **openfda.application_number**: Número de aplicación del medicamento.
- **openfda.brand_name**: Nombre de marca del medicamento.
- **openfda.generic_name**: Nombre genérico del medicamento.
- **openfda.manufacturer_name**: Nombre del fabricante del medicamento.
- **openfda.product_ndc**: Código Nacional de Medicamentos (NDC) del producto.
- **openfda.product_type**: Tipo de producto (e.g., humano, veterinario).
- **openfda.route**: Vía de administración del medicamento.
- **openfda.substance_name**: Nombre de la sustancia activa en el medicamento.
- **openfda.rxcui**: Identificador único de concepto de medicamento de RxNorm.
- **openfda.spl_id**: Identificador de la etiqueta del producto.
- **openfda.spl_set_id**: Identificador del conjunto de etiquetas del producto.
- **openfda.package_ndc**: Código NDC del paquete.
- **openfda.is_original_packager**: Indicador de si el producto es el envasador original.
- **openfda.upc**: Código Universal de Producto (UPC) del medicamento.
- **openfda.unii**: Identificador Único de Ingrediente (UNII) del medicamento.

Esta descripción detallada proporciona una visión clara de la información almacenada en cada atributo del JSON, lo que es esencial para preparar y utilizar adecuadamente los datos para entrenar un modelo transformer o realizar cualquier análisis adicional.

#https://coralogix.com/guides/opensearch/opensearch-serverless-start-3-steps/
#https://thenewstack.io/semantic-search-with-amazon-opensearch-serverless-and-titan/
#https://docs.aws.amazon.com/opensearch-service/latest/developerguide/serverless-sdk.html
#https://blog.stackademic.com/rag-using-llama3-langchain-and-chromadb-77bba0154df4

#https://www.sciencedirect.com/science/article/pii/S2352914822002763?ref=pdf_download&fr=RR-2&rr=8a80fcdb9bd174a6
#https://www.sciencedirect.com/science/article/pii/S1532046421001283
#https://jalammar.github.io/illustrated-bert/
#https://medium.com/@shaikhrayyan123/a-comprehensive-guide-to-understanding-bert-from-beginners-to-advanced-2379699e2b51
#https://sh-tsang.medium.com/review-bert-pre-training-of-deep-bidirectional-transformers-for-language-understanding-59b1684882db
#https://sh-tsang.medium.com/brief-review-biobert-a-pre-trained-biomedical-language-representation-model-for-biomedical-text-4b5cf07efdd7
#https://medium.com/nwamaka-imasogie/clinicalbert-using-deep-learning-transformer-model-to-predict-hospital-readmission-c82ff0e4bb03
#https://medium.com/nwamaka-imasogie/clinicalbert-using-deep-learning-transformer-model-to-predict-hospital-readmission-c82ff0e4bb03
#https://sh-tsang.medium.com/brief-review-clinial-bert-publicly-available-clinical-bert-embeddings-1026f2b04b92
#https://aclanthology.org/W19-1909/
#https://www.nature.com/articles/sdata201635


#https://dassum.medium.com/fine-tune-large-language-model-llm-on-a-custom-dataset-with-qlora-fb60abdeba07
#https://blog.stackademic.com/rag-using-llama3-langchain-and-chromadb-77bba0154df4
#https://www.youtube.com/watch?v=dzyDHMycx_c
#https://github.com/rohan-paul/LLM-FineTuning-Large-Language-Models/blob/main/Other-Language_Models_BERT_related/YT_Fine_tuning_BERT_NER_v1.ipynb
#https://github.com/rohan-paul/LLM-FineTuning-Large-Language-Models/blob/main/Llama-3_Finetuning_on_custom_dataset_with_unsloth.ipynb

#https://www.youtube.com/watch?v=P2m1kyGjAbA
#https://www.elastic.co/search-labs/blog/elasticsearch-rag-with-llama3-opensource-and-elastic