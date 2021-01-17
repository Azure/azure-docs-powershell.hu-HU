---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: f897c2adfe4154aeff5bd370437ea8b23e4efd36
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360497"
---
# <span data-ttu-id="69ea4-101">Invoke-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="69ea4-101">Invoke-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="69ea4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69ea4-102">SYNOPSIS</span></span>
<span data-ttu-id="69ea4-103">Adott műveleteket hív meg egy tárolón</span><span class="sxs-lookup"><span data-stu-id="69ea4-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="69ea4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="69ea4-104">SYNTAX</span></span>

### <span data-ttu-id="69ea4-105">InvokeByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="69ea4-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69ea4-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69ea4-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69ea4-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69ea4-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69ea4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="69ea4-108">DESCRIPTION</span></span>
<span data-ttu-id="69ea4-109">Az **Invoke-AzDataBoxEdgeStorageContainer** parancsmag műveleteket hoz létre egy adattároló adatfrissítéséhez egy Data Box Edge-eszközön.</span><span class="sxs-lookup"><span data-stu-id="69ea4-109">The **Invoke-AzDataBoxEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Data Box Edge device.</span></span> 

## <span data-ttu-id="69ea4-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="69ea4-110">EXAMPLES</span></span>

### <span data-ttu-id="69ea4-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="69ea4-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="69ea4-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="69ea4-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzDataBoxEdgeStorageContainer
```

## <span data-ttu-id="69ea4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69ea4-113">PARAMETERS</span></span>

### <span data-ttu-id="69ea4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69ea4-114">-AsJob</span></span>
<span data-ttu-id="69ea4-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="69ea4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69ea4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69ea4-116">-DefaultProfile</span></span>
<span data-ttu-id="69ea4-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69ea4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69ea4-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="69ea4-118">-DeviceName</span></span>
<span data-ttu-id="69ea4-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="69ea4-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ea4-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="69ea4-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="69ea4-121">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="69ea4-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ea4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69ea4-122">-InputObject</span></span>
<span data-ttu-id="69ea4-123">Meglévő EdgeStorageAccount objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="69ea4-123">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69ea4-124">-Name</span><span class="sxs-lookup"><span data-stu-id="69ea4-124">-Name</span></span>
<span data-ttu-id="69ea4-125">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="69ea4-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ea4-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69ea4-126">-PassThru</span></span>
<span data-ttu-id="69ea4-127">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="69ea4-127">returns true if successful</span></span>

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

### <span data-ttu-id="69ea4-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="69ea4-128">-RefreshData</span></span>
<span data-ttu-id="69ea4-129">A tároló metaadatainak frissítése a felhőből származó adatokkal</span><span class="sxs-lookup"><span data-stu-id="69ea4-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="69ea4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69ea4-130">-ResourceGroupName</span></span>
<span data-ttu-id="69ea4-131">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="69ea4-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ea4-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69ea4-132">-ResourceId</span></span>
<span data-ttu-id="69ea4-133">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="69ea4-133">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ea4-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69ea4-134">-Confirm</span></span>
<span data-ttu-id="69ea4-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="69ea4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69ea4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69ea4-136">-WhatIf</span></span>
<span data-ttu-id="69ea4-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="69ea4-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69ea4-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="69ea4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69ea4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69ea4-139">CommonParameters</span></span>
<span data-ttu-id="69ea4-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69ea4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69ea4-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69ea4-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69ea4-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69ea4-142">INPUTS</span></span>

### <span data-ttu-id="69ea4-143">System.String</span><span class="sxs-lookup"><span data-stu-id="69ea4-143">System.String</span></span>

### <span data-ttu-id="69ea4-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="69ea4-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="69ea4-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69ea4-145">OUTPUTS</span></span>

### <span data-ttu-id="69ea4-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="69ea4-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="69ea4-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="69ea4-147">NOTES</span></span>

## <span data-ttu-id="69ea4-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69ea4-148">RELATED LINKS</span></span>
