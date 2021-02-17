---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: 341edce877666d56a78064f1e13dc7b7af9b26a1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205943"
---
# <span data-ttu-id="a5333-101">Remove-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a5333-101">Remove-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="a5333-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5333-102">SYNOPSIS</span></span>
<span data-ttu-id="a5333-103">Távolítsa el a privát végpontkapcsolatot az Azure Cognitive Search szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="a5333-103">Remove the private endpoint connection from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="a5333-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a5333-104">SYNTAX</span></span>

### <span data-ttu-id="a5333-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a5333-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5333-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5333-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection -ParentObject <PSSearchService> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5333-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5333-107">InputObjectParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection -InputObject <PSPrivateEndpointConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5333-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5333-108">ResourceIdParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5333-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a5333-109">DESCRIPTION</span></span>
<span data-ttu-id="a5333-110">A **Remove-AzSearchPrivateEndpointConnection** eltávolítja a privát végpontkapcsolatot az Azure Cognitive Search szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="a5333-110">The **Remove-AzSearchPrivateEndpointConnection** removes the private endpoint connection from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="a5333-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a5333-111">EXAMPLES</span></span>

### <span data-ttu-id="a5333-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="a5333-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266
```

<span data-ttu-id="a5333-113">Ez a példa név szerint eltávolít egy privát végpontkapcsolatot a keresési szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="a5333-113">This example removes a private endpoint connection from the search service by name.</span></span>

## <span data-ttu-id="a5333-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5333-114">PARAMETERS</span></span>

### <span data-ttu-id="a5333-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5333-115">-DefaultProfile</span></span>
<span data-ttu-id="a5333-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5333-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5333-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a5333-117">-Force</span></span>
<span data-ttu-id="a5333-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a5333-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a5333-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5333-119">-InputObject</span></span>
<span data-ttu-id="a5333-120">Private endpoint connection input object</span><span class="sxs-lookup"><span data-stu-id="a5333-120">Private endpoint connection input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5333-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a5333-121">-Name</span></span>
<span data-ttu-id="a5333-122">Azure Kognitív keresési szolgáltatás – privát végpontkapcsolat neve</span><span class="sxs-lookup"><span data-stu-id="a5333-122">Azure Cognitive Search Service private endpoint connection name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5333-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a5333-123">-ParentObject</span></span>
<span data-ttu-id="a5333-124">Azure Kognitív keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="a5333-124">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5333-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5333-125">-PassThru</span></span>
<span data-ttu-id="a5333-126">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="a5333-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a5333-127">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="a5333-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a5333-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5333-128">-ResourceGroupName</span></span>
<span data-ttu-id="a5333-129">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a5333-129">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5333-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5333-130">-ResourceId</span></span>
<span data-ttu-id="a5333-131">Private link service resource id</span><span class="sxs-lookup"><span data-stu-id="a5333-131">Private link service resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5333-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a5333-132">-ServiceName</span></span>
<span data-ttu-id="a5333-133">Azure Kognitív keresési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="a5333-133">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5333-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5333-134">-Confirm</span></span>
<span data-ttu-id="a5333-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a5333-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5333-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5333-136">-WhatIf</span></span>
<span data-ttu-id="a5333-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a5333-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5333-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a5333-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5333-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5333-139">CommonParameters</span></span>
<span data-ttu-id="a5333-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5333-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5333-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5333-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5333-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5333-142">INPUTS</span></span>

### <span data-ttu-id="a5333-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="a5333-143">None</span></span>

## <span data-ttu-id="a5333-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5333-144">OUTPUTS</span></span>

### <span data-ttu-id="a5333-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a5333-145">System.Boolean</span></span>

## <span data-ttu-id="a5333-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a5333-146">NOTES</span></span>

## <span data-ttu-id="a5333-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5333-147">RELATED LINKS</span></span>

[<span data-ttu-id="a5333-148">Get-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="a5333-148">Get-AzSearchPrivateEndpointConnection.md</span></span>](./Get-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="a5333-149">Set-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="a5333-149">Set-AzSearchPrivateEndpointConnection.md</span></span>](./Set-AzSearchPrivateEndpointConnection.md)