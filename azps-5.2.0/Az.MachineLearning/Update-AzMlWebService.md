---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
ms.openlocfilehash: a170d21a2301541f1346905ed701d477ecba4204
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362500"
---
# <span data-ttu-id="bd23f-101">Update-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="bd23f-101">Update-AzMlWebService</span></span>

## <span data-ttu-id="bd23f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd23f-102">SYNOPSIS</span></span>
<span data-ttu-id="bd23f-103">Frissíti egy meglévő webszolgáltatás-erőforrás tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="bd23f-103">Updates properties of an existing web service resource.</span></span>

## <span data-ttu-id="bd23f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bd23f-104">SYNTAX</span></span>

### <span data-ttu-id="bd23f-105">UpdateFromParameters</span><span class="sxs-lookup"><span data-stu-id="bd23f-105">UpdateFromParameters</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd23f-106">UpdateFromObject</span><span class="sxs-lookup"><span data-stu-id="bd23f-106">UpdateFromObject</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd23f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bd23f-107">DESCRIPTION</span></span>
<span data-ttu-id="bd23f-108">A Update-AzMlWebService parancsmaggal frissítheti a webszolgáltatás nem statikus tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="bd23f-108">The Update-AzMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="bd23f-109">A parancsmag javításműveletként működik.</span><span class="sxs-lookup"><span data-stu-id="bd23f-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="bd23f-110">Csak a módosítani kívánt tulajdonságokat adja át.</span><span class="sxs-lookup"><span data-stu-id="bd23f-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="bd23f-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bd23f-111">EXAMPLES</span></span>

### <span data-ttu-id="bd23f-112">1. példa: Szelektív frissítési argumentumok</span><span class="sxs-lookup"><span data-stu-id="bd23f-112">Example 1: Selective update arguments</span></span>
```
Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="bd23f-113">Itt módosítjuk a leírást és az elsődleges hozzáférési kulcsot, és a webszolgáltatás futásidejű futásidejű nyomkövetési naplóihoz engedélyezik a diagnosztikai adatgyűjtést.</span><span class="sxs-lookup"><span data-stu-id="bd23f-113">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="bd23f-114">2. példa: Frissítés webszolgáltatás-példány alapján</span><span class="sxs-lookup"><span data-stu-id="bd23f-114">Example 2: Update based on a web service instance</span></span>
```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="bd23f-115">A példa először létrehoz egy olyan webszolgáltatás-definíciót, amely csak a frissíthető mezőket tartalmazza, majd felhívja a Update-AzMlWebService, hogy a ServiceUpdates paraméterrel alkalmazza őket.</span><span class="sxs-lookup"><span data-stu-id="bd23f-115">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="bd23f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd23f-116">PARAMETERS</span></span>

### <span data-ttu-id="bd23f-117">-Eszközök</span><span class="sxs-lookup"><span data-stu-id="bd23f-117">-Assets</span></span>
<span data-ttu-id="bd23f-118">A webszolgáltatást szolgáltató eszközök (például modulok, adatkészletek) halmaza.</span><span class="sxs-lookup"><span data-stu-id="bd23f-118">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd23f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd23f-119">-DefaultProfile</span></span>
<span data-ttu-id="bd23f-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bd23f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd23f-121">-Leírás</span><span class="sxs-lookup"><span data-stu-id="bd23f-121">-Description</span></span>
<span data-ttu-id="bd23f-122">A webszolgáltatás leírásának új értéke.</span><span class="sxs-lookup"><span data-stu-id="bd23f-122">The new value for the web service's description.</span></span>
<span data-ttu-id="bd23f-123">Ez látható a szolgáltatás Swagger API-sémában.</span><span class="sxs-lookup"><span data-stu-id="bd23f-123">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd23f-124">- Diagnosztika</span><span class="sxs-lookup"><span data-stu-id="bd23f-124">-Diagnostics</span></span>
<span data-ttu-id="bd23f-125">A webszolgáltatás diagnosztikai nyomkövetési gyűjteményét vezérlő beállítások.</span><span class="sxs-lookup"><span data-stu-id="bd23f-125">The settings that control the diagnostics traces collection for the web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.DiagnosticsConfiguration
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd23f-126">-Force</span><span class="sxs-lookup"><span data-stu-id="bd23f-126">-Force</span></span>
<span data-ttu-id="bd23f-127">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bd23f-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bd23f-128">-Input</span><span class="sxs-lookup"><span data-stu-id="bd23f-128">-Input</span></span>
<span data-ttu-id="bd23f-129">A webszolgáltatás által bevitt adatok definíciója, amely Swagger-sémastruktúraként van megtéve.</span><span class="sxs-lookup"><span data-stu-id="bd23f-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd23f-130">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="bd23f-130">-IsReadOnly</span></span>
<span data-ttu-id="bd23f-131">Azt adja meg, hogy a webszolgáltatás csak olvasható.</span><span class="sxs-lookup"><span data-stu-id="bd23f-131">Specifies that this web service is readonly.</span></span>
<span data-ttu-id="bd23f-132">A beállítás után a webszolgáltatás frissíthető, beleértve a tulajdonság értékét is, és csak törölhető.</span><span class="sxs-lookup"><span data-stu-id="bd23f-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd23f-133">-Keys</span><span class="sxs-lookup"><span data-stu-id="bd23f-133">-Keys</span></span>
<span data-ttu-id="bd23f-134">Frissíti a hívás hitelesítéséhez használt hozzáférési kulcsokat a szolgáltatás futásidejű API-ihoz.</span><span class="sxs-lookup"><span data-stu-id="bd23f-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd23f-135">-Name</span><span class="sxs-lookup"><span data-stu-id="bd23f-135">-Name</span></span>
<span data-ttu-id="bd23f-136">A frissíthető webszolgáltatás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="bd23f-136">The name of the web service resource to be updated.</span></span>

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

### <span data-ttu-id="bd23f-137">-Kimenet</span><span class="sxs-lookup"><span data-stu-id="bd23f-137">-Output</span></span>
<span data-ttu-id="bd23f-138">A webszolgáltatás kimenetének definíciója, amely egy Swagger sémastruktúraként van megtéve.</span><span class="sxs-lookup"><span data-stu-id="bd23f-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd23f-139">-Package</span><span class="sxs-lookup"><span data-stu-id="bd23f-139">-Package</span></span>
<span data-ttu-id="bd23f-140">A webszolgáltatást definiáló grafikoncsomag definíciója.</span><span class="sxs-lookup"><span data-stu-id="bd23f-140">The definition of the graph package that defines this web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.GraphPackage
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd23f-141">-Parameters</span><span class="sxs-lookup"><span data-stu-id="bd23f-141">-Parameters</span></span>
<span data-ttu-id="bd23f-142">A webszolgáltatáshoz definiált globális paraméterértékek halmaza, globális paraméternévként megadva – \> alapértelmezett értékgyűjtemény.</span><span class="sxs-lookup"><span data-stu-id="bd23f-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="bd23f-143">Ha nincs megadva alapértelmezett érték, a paramétert kötelezőnek tekintjük.</span><span class="sxs-lookup"><span data-stu-id="bd23f-143">If no default value is specified, the parameter is considered to be required.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd23f-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd23f-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="bd23f-145">A szolgáltatás valós idejű végpontjának konfigurációjának frissítései.</span><span class="sxs-lookup"><span data-stu-id="bd23f-145">Updates for the configuration of the service's realtime endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.RealtimeConfiguration
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd23f-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd23f-146">-ResourceGroupName</span></span>
<span data-ttu-id="bd23f-147">A frissíteni kívánt webszolgáltatást tartalmazó erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="bd23f-147">The resource group that contains the web service to be updated.</span></span>

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

### <span data-ttu-id="bd23f-148">-ServiceUpdates</span><span class="sxs-lookup"><span data-stu-id="bd23f-148">-ServiceUpdates</span></span>
<span data-ttu-id="bd23f-149">A webszolgáltatás-definíciós példányként biztosított webszolgáltatásra alkalmazandó frissítések.</span><span class="sxs-lookup"><span data-stu-id="bd23f-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="bd23f-150">Csak a nem statikus mezők módosulnak.</span><span class="sxs-lookup"><span data-stu-id="bd23f-150">Only non-static fields are modified.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: UpdateFromObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd23f-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="bd23f-151">-StorageAccountKey</span></span>
<span data-ttu-id="bd23f-152">A webszolgáltatáshoz társított tárfiók hozzáférési kulcsának elforgatása.</span><span class="sxs-lookup"><span data-stu-id="bd23f-152">Rotates the access key for the storage account associated with the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd23f-153">-Title</span><span class="sxs-lookup"><span data-stu-id="bd23f-153">-Title</span></span>
<span data-ttu-id="bd23f-154">A webszolgáltatás címének új értéke.</span><span class="sxs-lookup"><span data-stu-id="bd23f-154">The new value for the web service's title.</span></span>
<span data-ttu-id="bd23f-155">Ez látható a szolgáltatás Swagger API-sémában.</span><span class="sxs-lookup"><span data-stu-id="bd23f-155">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd23f-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd23f-156">-Confirm</span></span>
<span data-ttu-id="bd23f-157">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bd23f-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd23f-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd23f-158">-WhatIf</span></span>
<span data-ttu-id="bd23f-159">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bd23f-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd23f-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bd23f-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd23f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd23f-161">CommonParameters</span></span>
<span data-ttu-id="bd23f-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd23f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd23f-163">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd23f-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd23f-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd23f-164">INPUTS</span></span>

### <span data-ttu-id="bd23f-165">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="bd23f-165">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="bd23f-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd23f-166">OUTPUTS</span></span>

### <span data-ttu-id="bd23f-167">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="bd23f-167">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="bd23f-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bd23f-168">NOTES</span></span>
<span data-ttu-id="bd23f-169">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, gépi, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="bd23f-169">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="bd23f-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd23f-170">RELATED LINKS</span></span>
