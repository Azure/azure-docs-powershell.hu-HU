---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
ms.openlocfilehash: 75f94e5c93f81fa88dd33c3c0b94cb2b36ca291f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499995"
---
# <span data-ttu-id="7d42d-101">Update-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="7d42d-101">Update-AzureRmMlWebService</span></span>

## <span data-ttu-id="7d42d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7d42d-102">SYNOPSIS</span></span>
<span data-ttu-id="7d42d-103">Meglévő webszolgáltatás-erőforrás tulajdonságainak frissítése</span><span class="sxs-lookup"><span data-stu-id="7d42d-103">Updates properties of an existing web service resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d42d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7d42d-104">SYNTAX</span></span>

### <span data-ttu-id="7d42d-105">Frissítheti az adott tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="7d42d-105">Update specific properties of the .</span></span>
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d42d-106">Hozzon létre egy új Azure ML-webszolgáltatást egy webszolgáltatási példány-definícióból.</span><span class="sxs-lookup"><span data-stu-id="7d42d-106">Create a new Azure ML webservice from a WebService instance definition.</span></span>
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d42d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7d42d-107">DESCRIPTION</span></span>
<span data-ttu-id="7d42d-108">Az Update-AzureRmMlWebService parancsmag segítségével frissítheti egy webszolgáltatás nem statikus tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="7d42d-108">The Update-AzureRmMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="7d42d-109">A parancsmag a javítás műveletként működik.</span><span class="sxs-lookup"><span data-stu-id="7d42d-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="7d42d-110">Csak azokat a tulajdonságokat adja át, amelyeket módosítani szeretne.</span><span class="sxs-lookup"><span data-stu-id="7d42d-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="7d42d-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7d42d-111">EXAMPLES</span></span>

### <span data-ttu-id="7d42d-112">--------------------------Példa 1: szelektív frissítési argumentumok--------------------------</span><span class="sxs-lookup"><span data-stu-id="7d42d-112">--------------------------  Example 1: Selective update arguments  --------------------------</span></span>
<span data-ttu-id="7d42d-113">@ {bekezdés = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="7d42d-113">@{paragraph=PS C:\\\>}</span></span>





```
Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="7d42d-114">Itt cseréljük le a leírás, az elsődleges hozzáférés kulcsát, és engedélyeznie kell a diagnosztikai gyűjteményt minden nyomkövetéskor a webszolgáltatás futási időszaka alatt.</span><span class="sxs-lookup"><span data-stu-id="7d42d-114">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="7d42d-115">--------------------------Példa 2: frissítés webszolgáltatás-példányon alapuló--------------------------</span><span class="sxs-lookup"><span data-stu-id="7d42d-115">--------------------------  Example 2: Update based on a web service instance  --------------------------</span></span>
<span data-ttu-id="7d42d-116">@ {bekezdés = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="7d42d-116">@{paragraph=PS C:\\\>}</span></span>





```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="7d42d-117">A példa először létrehoz egy webszolgáltatás-definíciót, amely csak a frissítendő mezőket tartalmazza, majd a Update-AzureRmMlWebService kéri, hogy alkalmazza őket a ServiceUpdates paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="7d42d-117">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzureRmMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="7d42d-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7d42d-118">PARAMETERS</span></span>

### <span data-ttu-id="7d42d-119">-Eszközök</span><span class="sxs-lookup"><span data-stu-id="7d42d-119">-Assets</span></span>
<span data-ttu-id="7d42d-120">A webszolgáltatást alkotó eszközök (például modulok, adatkészletek).</span><span class="sxs-lookup"><span data-stu-id="7d42d-120">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d42d-121">-Leírás</span><span class="sxs-lookup"><span data-stu-id="7d42d-121">-Description</span></span>
<span data-ttu-id="7d42d-122">A webszolgáltatás leírásának új értéke.</span><span class="sxs-lookup"><span data-stu-id="7d42d-122">The new value for the web service's description.</span></span>
<span data-ttu-id="7d42d-123">Ez látható a szolgáltatás hencegő API-sémájában.</span><span class="sxs-lookup"><span data-stu-id="7d42d-123">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d42d-124">-Diagnosztika</span><span class="sxs-lookup"><span data-stu-id="7d42d-124">-Diagnostics</span></span>
<span data-ttu-id="7d42d-125">A webszolgáltatás diagnosztikai nyomkövetési gyűjteményét szabályozó beállítások.</span><span class="sxs-lookup"><span data-stu-id="7d42d-125">The settings that control the diagnostics traces collection for the web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.DiagnosticsConfiguration
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d42d-126">-Force</span><span class="sxs-lookup"><span data-stu-id="7d42d-126">-Force</span></span>
<span data-ttu-id="7d42d-127">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7d42d-127">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d42d-128">– Bemenet</span><span class="sxs-lookup"><span data-stu-id="7d42d-128">-Input</span></span>
<span data-ttu-id="7d42d-129">A webszolgáltatás bemenetének (ek) definíciója, a hencegő séma-konstrukcióban.</span><span class="sxs-lookup"><span data-stu-id="7d42d-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d42d-130">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="7d42d-130">-IsReadOnly</span></span>
<span data-ttu-id="7d42d-131">Megadja, hogy ez a webszolgáltatás írásvédett.</span><span class="sxs-lookup"><span data-stu-id="7d42d-131">Specifies that this web serviceis readonly.</span></span>
<span data-ttu-id="7d42d-132">Miután beállította, a webszolgáltatás már nem frissíthető, többek között a tulajdonság értékének módosítása, és csak törölhető.</span><span class="sxs-lookup"><span data-stu-id="7d42d-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d42d-133">-Billentyűk</span><span class="sxs-lookup"><span data-stu-id="7d42d-133">-Keys</span></span>
<span data-ttu-id="7d42d-134">A hívásoknak a szolgáltatás futásidejű API-khoz való hitelesítéséhez használt két hozzáférési kulcs (vagy mindkettő) frissítése</span><span class="sxs-lookup"><span data-stu-id="7d42d-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d42d-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7d42d-135">-Name</span></span>
<span data-ttu-id="7d42d-136">A frissítendő webszolgáltatás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="7d42d-136">The name of the web service resource to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d42d-137">-Output (kimenet)</span><span class="sxs-lookup"><span data-stu-id="7d42d-137">-Output</span></span>
<span data-ttu-id="7d42d-138">A webszolgáltatás kimenetének (s) definíciója, a hencegő séma-konstrukcióban.</span><span class="sxs-lookup"><span data-stu-id="7d42d-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d42d-139">-Package (csomag)</span><span class="sxs-lookup"><span data-stu-id="7d42d-139">-Package</span></span>
<span data-ttu-id="7d42d-140">A webszolgáltatás definiálására szolgáló Graph-csomag definíciója.</span><span class="sxs-lookup"><span data-stu-id="7d42d-140">The definition of the graph package that defines this web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.GraphPackage
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d42d-141">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="7d42d-141">-Parameters</span></span>
<span data-ttu-id="7d42d-142">A webes szolgáltatáshoz definiált globális paraméterek értéke, a globális paraméter neve – \> alapértelmezett érték gyűjtemény.</span><span class="sxs-lookup"><span data-stu-id="7d42d-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="7d42d-143">Ha nincs megadva alapértelmezett érték, akkor a paraméter szükségesnek tekintendő.</span><span class="sxs-lookup"><span data-stu-id="7d42d-143">If no default value is specified, the parameter is considered to be required.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d42d-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d42d-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="7d42d-145">A szolgáltatás valósidejű végpontjának konfigurációjának frissítései.</span><span class="sxs-lookup"><span data-stu-id="7d42d-145">Updates for the configuration of the service's realtime endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.RealtimeConfiguration
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d42d-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d42d-146">-ResourceGroupName</span></span>
<span data-ttu-id="7d42d-147">A frissítendő webszolgáltatás a frissítendő webszolgáltatást tartalmazó erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="7d42d-147">The resource group that contains the web service to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d42d-148">-ServiceUpdates</span><span class="sxs-lookup"><span data-stu-id="7d42d-148">-ServiceUpdates</span></span>
<span data-ttu-id="7d42d-149">Egy webszolgáltatás-definíciós példányként elérhető webszolgáltatásra érvényes módosítások halmaza.</span><span class="sxs-lookup"><span data-stu-id="7d42d-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="7d42d-150">Csak a nem statikus mezők módosulnak.</span><span class="sxs-lookup"><span data-stu-id="7d42d-150">Only non-static fields are modified.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Create a new Azure ML webservice from a WebService instance definition.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d42d-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7d42d-151">-StorageAccountKey</span></span>
<span data-ttu-id="7d42d-152">Elforgatja a webszolgáltatáshoz társított tárterület elérési útjának elérési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="7d42d-152">Rotates the access key for the storage account associated with the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d42d-153">-Cím</span><span class="sxs-lookup"><span data-stu-id="7d42d-153">-Title</span></span>
<span data-ttu-id="7d42d-154">A webszolgáltatás címének új értéke.</span><span class="sxs-lookup"><span data-stu-id="7d42d-154">The new value for the web service's title.</span></span>
<span data-ttu-id="7d42d-155">Ez látható a szolgáltatás hencegő API-sémájában.</span><span class="sxs-lookup"><span data-stu-id="7d42d-155">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d42d-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7d42d-156">-Confirm</span></span>
<span data-ttu-id="7d42d-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7d42d-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d42d-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d42d-158">-WhatIf</span></span>
<span data-ttu-id="7d42d-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7d42d-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d42d-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7d42d-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d42d-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d42d-161">-DefaultProfile</span></span>
<span data-ttu-id="7d42d-162">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7d42d-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d42d-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d42d-163">CommonParameters</span></span>
<span data-ttu-id="7d42d-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7d42d-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d42d-165">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d42d-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d42d-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d42d-166">INPUTS</span></span>

### <span data-ttu-id="7d42d-167">WebService</span><span class="sxs-lookup"><span data-stu-id="7d42d-167">WebService</span></span>
<span data-ttu-id="7d42d-168">A ' ServiceUpdates ' paraméter a "webszolgáltatás" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="7d42d-168">Parameter 'ServiceUpdates' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="7d42d-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d42d-169">OUTPUTS</span></span>

### <span data-ttu-id="7d42d-170">Microsoft. Azure. Management. MachineLearning. WebServices. models. webszolgáltatás</span><span class="sxs-lookup"><span data-stu-id="7d42d-170">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="7d42d-171">Az Azure Machine learning webszolgáltatás összefoglaló leírása.</span><span class="sxs-lookup"><span data-stu-id="7d42d-171">A summary description of the Azure Machine Learning web service.</span></span>
<span data-ttu-id="7d42d-172">Hasonló a visszaadott leíráshoz, ha az Get-AzureRmMlWebService parancsmagot egy meglévő webszolgáltatásban hívja fel.</span><span class="sxs-lookup"><span data-stu-id="7d42d-172">Similar to the description returned by calling the Get-AzureRmMlWebService cmdlet on an existing web service.</span></span>
<span data-ttu-id="7d42d-173">Ez a leírás nem tartalmaz bizalmas tulajdonságokat, például a tárolási fiók hitelesítő adatait és a szolgáltatás elérési kulcsait.</span><span class="sxs-lookup"><span data-stu-id="7d42d-173">This description does not contain sensitive properties such as storage account's credentials and the service's access keys.</span></span>

## <span data-ttu-id="7d42d-174">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7d42d-174">NOTES</span></span>
<span data-ttu-id="7d42d-175">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="7d42d-175">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="7d42d-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d42d-176">RELATED LINKS</span></span>

