---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/update-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
ms.openlocfilehash: 5fb8c8f71366dd9fd0a2c6b12fc023c1ce3ccf9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502559"
---
# <span data-ttu-id="1ae7f-101">Update-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="1ae7f-101">Update-AzureRmMlWebService</span></span>

## <span data-ttu-id="1ae7f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ae7f-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae7f-103">Meglévő webszolgáltatás-erőforrás tulajdonságainak frissítése</span><span class="sxs-lookup"><span data-stu-id="1ae7f-103">Updates properties of an existing web service resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ae7f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ae7f-104">SYNTAX</span></span>

### <span data-ttu-id="1ae7f-105">UpdateFromParameters</span><span class="sxs-lookup"><span data-stu-id="1ae7f-105">UpdateFromParameters</span></span>
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ae7f-106">UpdateFromObject</span><span class="sxs-lookup"><span data-stu-id="1ae7f-106">UpdateFromObject</span></span>
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ae7f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ae7f-107">DESCRIPTION</span></span>
<span data-ttu-id="1ae7f-108">Az Update-AzureRmMlWebService parancsmag segítségével frissítheti egy webszolgáltatás nem statikus tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-108">The Update-AzureRmMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="1ae7f-109">A parancsmag a javítás műveletként működik.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="1ae7f-110">Csak azokat a tulajdonságokat adja át, amelyeket módosítani szeretne.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="1ae7f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="1ae7f-111">EXAMPLES</span></span>

### <span data-ttu-id="1ae7f-112">--------------------------Példa 1: szelektív frissítési argumentumok--------------------------</span><span class="sxs-lookup"><span data-stu-id="1ae7f-112">--------------------------  Example 1: Selective update arguments  --------------------------</span></span>
```
Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="1ae7f-113">Itt cseréljük le a leírás, az elsődleges hozzáférés kulcsát, és engedélyeznie kell a diagnosztikai gyűjteményt minden nyomkövetéskor a webszolgáltatás futási időszaka alatt.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-113">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="1ae7f-114">--------------------------Példa 2: frissítés webszolgáltatás-példányon alapuló--------------------------</span><span class="sxs-lookup"><span data-stu-id="1ae7f-114">--------------------------  Example 2: Update based on a web service instance  --------------------------</span></span>
```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="1ae7f-115">A példa először létrehoz egy webszolgáltatás-definíciót, amely csak a frissítendő mezőket tartalmazza, majd a Update-AzureRmMlWebService kéri, hogy alkalmazza őket a ServiceUpdates paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-115">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzureRmMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="1ae7f-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ae7f-116">PARAMETERS</span></span>

### <span data-ttu-id="1ae7f-117">-Eszközök</span><span class="sxs-lookup"><span data-stu-id="1ae7f-117">-Assets</span></span>
<span data-ttu-id="1ae7f-118">A webszolgáltatást alkotó eszközök (például modulok, adatkészletek).</span><span class="sxs-lookup"><span data-stu-id="1ae7f-118">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

```yaml
Type: Hashtable
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae7f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae7f-119">-DefaultProfile</span></span>
<span data-ttu-id="1ae7f-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1ae7f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae7f-121">-Leírás</span><span class="sxs-lookup"><span data-stu-id="1ae7f-121">-Description</span></span>
<span data-ttu-id="1ae7f-122">A webszolgáltatás leírásának új értéke.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-122">The new value for the web service's description.</span></span>
<span data-ttu-id="1ae7f-123">Ez látható a szolgáltatás hencegő API-sémájában.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-123">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: String
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae7f-124">-Diagnosztika</span><span class="sxs-lookup"><span data-stu-id="1ae7f-124">-Diagnostics</span></span>
<span data-ttu-id="1ae7f-125">A webszolgáltatás diagnosztikai nyomkövetési gyűjteményét szabályozó beállítások.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-125">The settings that control the diagnostics traces collection for the web service.</span></span>

```yaml
Type: DiagnosticsConfiguration
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae7f-126">-Force</span><span class="sxs-lookup"><span data-stu-id="1ae7f-126">-Force</span></span>
<span data-ttu-id="1ae7f-127">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-127">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae7f-128">– Bemenet</span><span class="sxs-lookup"><span data-stu-id="1ae7f-128">-Input</span></span>
<span data-ttu-id="1ae7f-129">A webszolgáltatás bemenetének (ek) definíciója, a hencegő séma-konstrukcióban.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae7f-130">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="1ae7f-130">-IsReadOnly</span></span>
<span data-ttu-id="1ae7f-131">Megadja, hogy ez a webszolgáltatás írásvédett.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-131">Specifies that this web serviceis readonly.</span></span>
<span data-ttu-id="1ae7f-132">Miután beállította, a webszolgáltatás már nem frissíthető, többek között a tulajdonság értékének módosítása, és csak törölhető.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae7f-133">-Billentyűk</span><span class="sxs-lookup"><span data-stu-id="1ae7f-133">-Keys</span></span>
<span data-ttu-id="1ae7f-134">A hívásoknak a szolgáltatás futásidejű API-khoz való hitelesítéséhez használt két hozzáférési kulcs (vagy mindkettő) frissítése</span><span class="sxs-lookup"><span data-stu-id="1ae7f-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

```yaml
Type: WebServiceKeys
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae7f-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1ae7f-135">-Name</span></span>
<span data-ttu-id="1ae7f-136">A frissítendő webszolgáltatás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-136">The name of the web service resource to be updated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae7f-137">-Output (kimenet)</span><span class="sxs-lookup"><span data-stu-id="1ae7f-137">-Output</span></span>
<span data-ttu-id="1ae7f-138">A webszolgáltatás kimenetének (s) definíciója, a hencegő séma-konstrukcióban.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae7f-139">-Package (csomag)</span><span class="sxs-lookup"><span data-stu-id="1ae7f-139">-Package</span></span>
<span data-ttu-id="1ae7f-140">A webszolgáltatás definiálására szolgáló Graph-csomag definíciója.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-140">The definition of the graph package that defines this web service.</span></span>

```yaml
Type: GraphPackage
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae7f-141">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="1ae7f-141">-Parameters</span></span>
<span data-ttu-id="1ae7f-142">A webes szolgáltatáshoz definiált globális paraméterek értéke, a globális paraméter neve – \> alapértelmezett érték gyűjtemény.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="1ae7f-143">Ha nincs megadva alapértelmezett érték, akkor a paraméter szükségesnek tekintendő.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-143">If no default value is specified, the parameter is considered to be required.</span></span>

```yaml
Type: Hashtable
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae7f-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ae7f-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="1ae7f-145">A szolgáltatás valósidejű végpontjának konfigurációjának frissítései.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-145">Updates for the configuration of the service's realtime endpoint.</span></span>

```yaml
Type: RealtimeConfiguration
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae7f-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ae7f-146">-ResourceGroupName</span></span>
<span data-ttu-id="1ae7f-147">A frissítendő webszolgáltatás a frissítendő webszolgáltatást tartalmazó erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-147">The resource group that contains the web service to be updated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae7f-148">-ServiceUpdates</span><span class="sxs-lookup"><span data-stu-id="1ae7f-148">-ServiceUpdates</span></span>
<span data-ttu-id="1ae7f-149">Egy webszolgáltatás-definíciós példányként elérhető webszolgáltatásra érvényes módosítások halmaza.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="1ae7f-150">Csak a nem statikus mezők módosulnak.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-150">Only non-static fields are modified.</span></span>

```yaml
Type: WebService
Parameter Sets: UpdateFromObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae7f-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="1ae7f-151">-StorageAccountKey</span></span>
<span data-ttu-id="1ae7f-152">Elforgatja a webszolgáltatáshoz társított tárterület elérési útjának elérési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-152">Rotates the access key for the storage account associated with the web service.</span></span>

```yaml
Type: String
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae7f-153">-Cím</span><span class="sxs-lookup"><span data-stu-id="1ae7f-153">-Title</span></span>
<span data-ttu-id="1ae7f-154">A webszolgáltatás címének új értéke.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-154">The new value for the web service's title.</span></span>
<span data-ttu-id="1ae7f-155">Ez látható a szolgáltatás hencegő API-sémájában.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-155">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: String
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae7f-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1ae7f-156">-Confirm</span></span>
<span data-ttu-id="1ae7f-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae7f-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ae7f-158">-WhatIf</span></span>
<span data-ttu-id="1ae7f-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ae7f-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-160">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae7f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae7f-161">CommonParameters</span></span>
<span data-ttu-id="1ae7f-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1ae7f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae7f-163">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ae7f-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae7f-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ae7f-164">INPUTS</span></span>

### <span data-ttu-id="1ae7f-165">WebService</span><span class="sxs-lookup"><span data-stu-id="1ae7f-165">WebService</span></span>
<span data-ttu-id="1ae7f-166">A ' ServiceUpdates ' paraméter a "webszolgáltatás" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="1ae7f-166">Parameter 'ServiceUpdates' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="1ae7f-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ae7f-167">OUTPUTS</span></span>

### <span data-ttu-id="1ae7f-168">Microsoft. Azure. Management. MachineLearning. WebServices. models. webszolgáltatás</span><span class="sxs-lookup"><span data-stu-id="1ae7f-168">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="1ae7f-169">Az Azure Machine learning webszolgáltatás összefoglaló leírása.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-169">A summary description of the Azure Machine Learning web service.</span></span>
<span data-ttu-id="1ae7f-170">Hasonló a visszaadott leíráshoz, ha az Get-AzureRmMlWebService parancsmagot egy meglévő webszolgáltatásban hívja fel.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-170">Similar to the description returned by calling the Get-AzureRmMlWebService cmdlet on an existing web service.</span></span>
<span data-ttu-id="1ae7f-171">Ez a leírás nem tartalmaz bizalmas tulajdonságokat, például a tárolási fiók hitelesítő adatait és a szolgáltatás elérési kulcsait.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-171">This description does not contain sensitive properties such as storage account's credentials and the service's access keys.</span></span>

## <span data-ttu-id="1ae7f-172">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ae7f-172">NOTES</span></span>
<span data-ttu-id="1ae7f-173">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="1ae7f-173">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="1ae7f-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ae7f-174">RELATED LINKS</span></span>

