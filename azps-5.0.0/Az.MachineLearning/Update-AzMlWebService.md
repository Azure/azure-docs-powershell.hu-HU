---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
ms.openlocfilehash: a170d21a2301541f1346905ed701d477ecba4204
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194628"
---
# <span data-ttu-id="1f693-101">Update-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="1f693-101">Update-AzMlWebService</span></span>

## <span data-ttu-id="1f693-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f693-102">SYNOPSIS</span></span>
<span data-ttu-id="1f693-103">Meglévő webszolgáltatás-erőforrás tulajdonságainak frissítése</span><span class="sxs-lookup"><span data-stu-id="1f693-103">Updates properties of an existing web service resource.</span></span>

## <span data-ttu-id="1f693-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f693-104">SYNTAX</span></span>

### <span data-ttu-id="1f693-105">UpdateFromParameters</span><span class="sxs-lookup"><span data-stu-id="1f693-105">UpdateFromParameters</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f693-106">UpdateFromObject</span><span class="sxs-lookup"><span data-stu-id="1f693-106">UpdateFromObject</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f693-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f693-107">DESCRIPTION</span></span>
<span data-ttu-id="1f693-108">Az Update-AzMlWebService parancsmag segítségével frissítheti egy webszolgáltatás nem statikus tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="1f693-108">The Update-AzMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="1f693-109">A parancsmag a javítás műveletként működik.</span><span class="sxs-lookup"><span data-stu-id="1f693-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="1f693-110">Csak azokat a tulajdonságokat adja át, amelyeket módosítani szeretne.</span><span class="sxs-lookup"><span data-stu-id="1f693-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="1f693-111">Példák</span><span class="sxs-lookup"><span data-stu-id="1f693-111">EXAMPLES</span></span>

### <span data-ttu-id="1f693-112">Példa 1: szelektív frissítési argumentumok</span><span class="sxs-lookup"><span data-stu-id="1f693-112">Example 1: Selective update arguments</span></span>
```
Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="1f693-113">Itt cseréljük le a leírás, az elsődleges hozzáférés kulcsát, és engedélyeznie kell a diagnosztikai gyűjteményt minden nyomkövetéskor a webszolgáltatás futási időszaka alatt.</span><span class="sxs-lookup"><span data-stu-id="1f693-113">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="1f693-114">2. példa: webszolgáltatás-példányon alapuló frissítés</span><span class="sxs-lookup"><span data-stu-id="1f693-114">Example 2: Update based on a web service instance</span></span>
```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="1f693-115">A példa először létrehoz egy webszolgáltatás-definíciót, amely csak a frissítendő mezőket tartalmazza, majd a Update-AzMlWebService kéri, hogy alkalmazza őket a ServiceUpdates paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="1f693-115">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="1f693-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f693-116">PARAMETERS</span></span>

### <span data-ttu-id="1f693-117">-Eszközök</span><span class="sxs-lookup"><span data-stu-id="1f693-117">-Assets</span></span>
<span data-ttu-id="1f693-118">A webszolgáltatást alkotó eszközök (például modulok, adatkészletek).</span><span class="sxs-lookup"><span data-stu-id="1f693-118">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

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

### <span data-ttu-id="1f693-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f693-119">-DefaultProfile</span></span>
<span data-ttu-id="1f693-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1f693-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f693-121">-Leírás</span><span class="sxs-lookup"><span data-stu-id="1f693-121">-Description</span></span>
<span data-ttu-id="1f693-122">A webszolgáltatás leírásának új értéke.</span><span class="sxs-lookup"><span data-stu-id="1f693-122">The new value for the web service's description.</span></span>
<span data-ttu-id="1f693-123">Ez látható a szolgáltatás hencegő API-sémájában.</span><span class="sxs-lookup"><span data-stu-id="1f693-123">This is visible in the service's Swagger API schema.</span></span>

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

### <span data-ttu-id="1f693-124">-Diagnosztika</span><span class="sxs-lookup"><span data-stu-id="1f693-124">-Diagnostics</span></span>
<span data-ttu-id="1f693-125">A webszolgáltatás diagnosztikai nyomkövetési gyűjteményét szabályozó beállítások.</span><span class="sxs-lookup"><span data-stu-id="1f693-125">The settings that control the diagnostics traces collection for the web service.</span></span>

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

### <span data-ttu-id="1f693-126">-Force</span><span class="sxs-lookup"><span data-stu-id="1f693-126">-Force</span></span>
<span data-ttu-id="1f693-127">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1f693-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1f693-128">– Bemenet</span><span class="sxs-lookup"><span data-stu-id="1f693-128">-Input</span></span>
<span data-ttu-id="1f693-129">A webszolgáltatás bemenetének (ek) definíciója, a hencegő séma-konstrukcióban.</span><span class="sxs-lookup"><span data-stu-id="1f693-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

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

### <span data-ttu-id="1f693-130">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="1f693-130">-IsReadOnly</span></span>
<span data-ttu-id="1f693-131">Megadja, hogy ez a webszolgáltatás írásvédett.</span><span class="sxs-lookup"><span data-stu-id="1f693-131">Specifies that this web service is readonly.</span></span>
<span data-ttu-id="1f693-132">Miután beállította, a webszolgáltatás már nem frissíthető, többek között a tulajdonság értékének módosítása, és csak törölhető.</span><span class="sxs-lookup"><span data-stu-id="1f693-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

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

### <span data-ttu-id="1f693-133">-Billentyűk</span><span class="sxs-lookup"><span data-stu-id="1f693-133">-Keys</span></span>
<span data-ttu-id="1f693-134">A hívásoknak a szolgáltatás futásidejű API-khoz való hitelesítéséhez használt két hozzáférési kulcs (vagy mindkettő) frissítése</span><span class="sxs-lookup"><span data-stu-id="1f693-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

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

### <span data-ttu-id="1f693-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1f693-135">-Name</span></span>
<span data-ttu-id="1f693-136">A frissítendő webszolgáltatás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="1f693-136">The name of the web service resource to be updated.</span></span>

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

### <span data-ttu-id="1f693-137">-Output (kimenet)</span><span class="sxs-lookup"><span data-stu-id="1f693-137">-Output</span></span>
<span data-ttu-id="1f693-138">A webszolgáltatás kimenetének (s) definíciója, a hencegő séma-konstrukcióban.</span><span class="sxs-lookup"><span data-stu-id="1f693-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

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

### <span data-ttu-id="1f693-139">-Package (csomag)</span><span class="sxs-lookup"><span data-stu-id="1f693-139">-Package</span></span>
<span data-ttu-id="1f693-140">A webszolgáltatás definiálására szolgáló Graph-csomag definíciója.</span><span class="sxs-lookup"><span data-stu-id="1f693-140">The definition of the graph package that defines this web service.</span></span>

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

### <span data-ttu-id="1f693-141">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="1f693-141">-Parameters</span></span>
<span data-ttu-id="1f693-142">A webes szolgáltatáshoz definiált globális paraméterek értéke, a globális paraméter neve – \> alapértelmezett érték gyűjtemény.</span><span class="sxs-lookup"><span data-stu-id="1f693-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="1f693-143">Ha nincs megadva alapértelmezett érték, akkor a paraméter szükségesnek tekintendő.</span><span class="sxs-lookup"><span data-stu-id="1f693-143">If no default value is specified, the parameter is considered to be required.</span></span>

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

### <span data-ttu-id="1f693-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="1f693-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="1f693-145">A szolgáltatás valósidejű végpontjának konfigurációjának frissítései.</span><span class="sxs-lookup"><span data-stu-id="1f693-145">Updates for the configuration of the service's realtime endpoint.</span></span>

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

### <span data-ttu-id="1f693-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f693-146">-ResourceGroupName</span></span>
<span data-ttu-id="1f693-147">A frissítendő webszolgáltatás a frissítendő webszolgáltatást tartalmazó erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="1f693-147">The resource group that contains the web service to be updated.</span></span>

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

### <span data-ttu-id="1f693-148">-ServiceUpdates</span><span class="sxs-lookup"><span data-stu-id="1f693-148">-ServiceUpdates</span></span>
<span data-ttu-id="1f693-149">Egy webszolgáltatás-definíciós példányként elérhető webszolgáltatásra érvényes módosítások halmaza.</span><span class="sxs-lookup"><span data-stu-id="1f693-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="1f693-150">Csak a nem statikus mezők módosulnak.</span><span class="sxs-lookup"><span data-stu-id="1f693-150">Only non-static fields are modified.</span></span>

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

### <span data-ttu-id="1f693-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="1f693-151">-StorageAccountKey</span></span>
<span data-ttu-id="1f693-152">Elforgatja a webszolgáltatáshoz társított tárterület elérési útjának elérési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="1f693-152">Rotates the access key for the storage account associated with the web service.</span></span>

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

### <span data-ttu-id="1f693-153">-Cím</span><span class="sxs-lookup"><span data-stu-id="1f693-153">-Title</span></span>
<span data-ttu-id="1f693-154">A webszolgáltatás címének új értéke.</span><span class="sxs-lookup"><span data-stu-id="1f693-154">The new value for the web service's title.</span></span>
<span data-ttu-id="1f693-155">Ez látható a szolgáltatás hencegő API-sémájában.</span><span class="sxs-lookup"><span data-stu-id="1f693-155">This is visible in the service's Swagger API schema.</span></span>

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

### <span data-ttu-id="1f693-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1f693-156">-Confirm</span></span>
<span data-ttu-id="1f693-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1f693-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f693-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f693-158">-WhatIf</span></span>
<span data-ttu-id="1f693-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1f693-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f693-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1f693-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f693-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f693-161">CommonParameters</span></span>
<span data-ttu-id="1f693-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f693-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f693-163">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f693-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f693-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f693-164">INPUTS</span></span>

### <span data-ttu-id="1f693-165">Microsoft. Azure. Management. MachineLearning. WebServices. models. webszolgáltatás</span><span class="sxs-lookup"><span data-stu-id="1f693-165">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="1f693-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f693-166">OUTPUTS</span></span>

### <span data-ttu-id="1f693-167">Microsoft. Azure. Management. MachineLearning. WebServices. models. webszolgáltatás</span><span class="sxs-lookup"><span data-stu-id="1f693-167">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="1f693-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f693-168">NOTES</span></span>
<span data-ttu-id="1f693-169">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="1f693-169">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="1f693-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f693-170">RELATED LINKS</span></span>
