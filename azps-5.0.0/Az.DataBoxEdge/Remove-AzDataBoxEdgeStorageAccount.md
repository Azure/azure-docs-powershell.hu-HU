---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 1f8e20b826a477778de5325ff147cbd7ad28a9fb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298697"
---
# <span data-ttu-id="fa8ac-101">Remove-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fa8ac-101">Remove-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="fa8ac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fa8ac-102">SYNOPSIS</span></span>
<span data-ttu-id="fa8ac-103">Eltávolítja az eszköz Edge Storage-fiókját.</span><span class="sxs-lookup"><span data-stu-id="fa8ac-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="fa8ac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fa8ac-104">SYNTAX</span></span>

### <span data-ttu-id="fa8ac-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fa8ac-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa8ac-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa8ac-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa8ac-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa8ac-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-InputObject] <PSDataBoxEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa8ac-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fa8ac-108">DESCRIPTION</span></span>
<span data-ttu-id="fa8ac-109">A **Remove-AzDataBoxEdgeStorageAccount** parancsmag eltávolítja a kapcsolódó peremhálózat-tároló fiókot az adatmező Edge-eszközéhez.</span><span class="sxs-lookup"><span data-stu-id="fa8ac-109">The **Remove-AzDataBoxEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Data Box Edge device.</span></span> <span data-ttu-id="fa8ac-110">Megadhatja az Edge-tároló fiók nevét, amelyet a parancsmag paraméterként szeretne eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="fa8ac-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="fa8ac-111">Példák</span><span class="sxs-lookup"><span data-stu-id="fa8ac-111">EXAMPLES</span></span>

### <span data-ttu-id="fa8ac-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fa8ac-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="fa8ac-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fa8ac-113">PARAMETERS</span></span>

### <span data-ttu-id="fa8ac-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa8ac-114">-AsJob</span></span>
<span data-ttu-id="fa8ac-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fa8ac-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa8ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa8ac-116">-DefaultProfile</span></span>
<span data-ttu-id="fa8ac-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fa8ac-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa8ac-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="fa8ac-118">-DeviceName</span></span>
<span data-ttu-id="fa8ac-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="fa8ac-119">Device Name</span></span>

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

### <span data-ttu-id="fa8ac-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa8ac-120">-InputObject</span></span>
<span data-ttu-id="fa8ac-121">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="fa8ac-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa8ac-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fa8ac-122">-Name</span></span>
<span data-ttu-id="fa8ac-123">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="fa8ac-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa8ac-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa8ac-124">-PassThru</span></span>
<span data-ttu-id="fa8ac-125">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="fa8ac-125">returns true if successful</span></span>

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

### <span data-ttu-id="fa8ac-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa8ac-126">-ResourceGroupName</span></span>
<span data-ttu-id="fa8ac-127">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="fa8ac-127">Resource Group Name</span></span>

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

### <span data-ttu-id="fa8ac-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa8ac-128">-ResourceId</span></span>
<span data-ttu-id="fa8ac-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa8ac-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="fa8ac-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fa8ac-130">-Confirm</span></span>
<span data-ttu-id="fa8ac-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fa8ac-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa8ac-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa8ac-132">-WhatIf</span></span>
<span data-ttu-id="fa8ac-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fa8ac-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa8ac-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fa8ac-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa8ac-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa8ac-135">CommonParameters</span></span>
<span data-ttu-id="fa8ac-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fa8ac-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa8ac-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fa8ac-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa8ac-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa8ac-138">INPUTS</span></span>

### <span data-ttu-id="fa8ac-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fa8ac-139">System.String</span></span>

### <span data-ttu-id="fa8ac-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fa8ac-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="fa8ac-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa8ac-141">OUTPUTS</span></span>

### <span data-ttu-id="fa8ac-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fa8ac-142">System.Boolean</span></span>

## <span data-ttu-id="fa8ac-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fa8ac-143">NOTES</span></span>

## <span data-ttu-id="fa8ac-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa8ac-144">RELATED LINKS</span></span>
