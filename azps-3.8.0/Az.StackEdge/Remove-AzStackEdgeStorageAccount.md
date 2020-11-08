---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
ms.openlocfilehash: d4b815e0caa85bee26086f475f86e1757b690fbd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013908"
---
# <span data-ttu-id="39528-101">Remove-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39528-101">Remove-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="39528-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="39528-102">SYNOPSIS</span></span>
<span data-ttu-id="39528-103">Eltávolítja az eszköz Edge Storage-fiókját.</span><span class="sxs-lookup"><span data-stu-id="39528-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="39528-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="39528-104">SYNTAX</span></span>

### <span data-ttu-id="39528-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="39528-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39528-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39528-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39528-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39528-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-InputObject] <PSStackEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39528-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="39528-108">DESCRIPTION</span></span>
<span data-ttu-id="39528-109">A **Remove-AzStackEdgeStorageAccount** parancsmag eltávolítja a kapcsolódó peremhálózat-tároló fiókot a halom szélén álló eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="39528-109">The **Remove-AzStackEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Stack Edge device.</span></span> <span data-ttu-id="39528-110">Megadhatja az Edge-tároló fiók nevét, amelyet a parancsmag paraméterként szeretne eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="39528-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="39528-111">Példák</span><span class="sxs-lookup"><span data-stu-id="39528-111">EXAMPLES</span></span>

### <span data-ttu-id="39528-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="39528-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="39528-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="39528-113">PARAMETERS</span></span>

### <span data-ttu-id="39528-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39528-114">-AsJob</span></span>
<span data-ttu-id="39528-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="39528-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39528-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39528-116">-DefaultProfile</span></span>
<span data-ttu-id="39528-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39528-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39528-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="39528-118">-DeviceName</span></span>
<span data-ttu-id="39528-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="39528-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39528-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39528-120">-InputObject</span></span>
<span data-ttu-id="39528-121">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="39528-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeStorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39528-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="39528-122">-Name</span></span>
<span data-ttu-id="39528-123">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="39528-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeStorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39528-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39528-124">-PassThru</span></span>
<span data-ttu-id="39528-125">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="39528-125">returns true if successful</span></span>

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

### <span data-ttu-id="39528-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39528-126">-ResourceGroupName</span></span>
<span data-ttu-id="39528-127">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="39528-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39528-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39528-128">-ResourceId</span></span>
<span data-ttu-id="39528-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="39528-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39528-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="39528-130">-Confirm</span></span>
<span data-ttu-id="39528-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="39528-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39528-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39528-132">-WhatIf</span></span>
<span data-ttu-id="39528-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="39528-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39528-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="39528-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39528-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39528-135">CommonParameters</span></span>
<span data-ttu-id="39528-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="39528-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39528-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="39528-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39528-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="39528-138">INPUTS</span></span>

### <span data-ttu-id="39528-139">System. String</span><span class="sxs-lookup"><span data-stu-id="39528-139">System.String</span></span>

### <span data-ttu-id="39528-140">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39528-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="39528-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39528-141">OUTPUTS</span></span>

### <span data-ttu-id="39528-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="39528-142">System.Boolean</span></span>

## <span data-ttu-id="39528-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="39528-143">NOTES</span></span>

## <span data-ttu-id="39528-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39528-144">RELATED LINKS</span></span>
