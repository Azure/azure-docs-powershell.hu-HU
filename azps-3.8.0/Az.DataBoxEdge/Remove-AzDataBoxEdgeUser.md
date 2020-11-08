---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
ms.openlocfilehash: cecfa3e009f6d6fbc7167c4b8f1ca110d547b5b7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014557"
---
# <span data-ttu-id="c6c48-101">Remove-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="c6c48-101">Remove-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="c6c48-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c6c48-102">SYNOPSIS</span></span>
<span data-ttu-id="c6c48-103">Eltávolít egy felhasználót egy eszközön.</span><span class="sxs-lookup"><span data-stu-id="c6c48-103">Removes a user on a device.</span></span>

## <span data-ttu-id="c6c48-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c6c48-104">SYNTAX</span></span>

### <span data-ttu-id="c6c48-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c6c48-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6c48-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6c48-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6c48-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6c48-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-InputObject] <PSDataBoxEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6c48-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c6c48-108">DESCRIPTION</span></span>
<span data-ttu-id="c6c48-109">A **Remove-AzDataBoxEdgeUser** parancsmag eltávolítja a felhasználót az adatmező szélén lévő eszközön.</span><span class="sxs-lookup"><span data-stu-id="c6c48-109">The **Remove-AzDataBoxEdgeUser** cmdlet removes a user on the Data Box Edge device.</span></span> <span data-ttu-id="c6c48-110">Csak a típusú felhasználók létrehozása `Share` támogatott.</span><span class="sxs-lookup"><span data-stu-id="c6c48-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="c6c48-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c6c48-111">EXAMPLES</span></span>

### <span data-ttu-id="c6c48-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c6c48-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="c6c48-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c6c48-113">PARAMETERS</span></span>

### <span data-ttu-id="c6c48-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6c48-114">-AsJob</span></span>
<span data-ttu-id="c6c48-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c6c48-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c6c48-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6c48-116">-DefaultProfile</span></span>
<span data-ttu-id="c6c48-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c6c48-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6c48-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c6c48-118">-DeviceName</span></span>
<span data-ttu-id="c6c48-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="c6c48-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6c48-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6c48-120">-InputObject</span></span>
<span data-ttu-id="c6c48-121">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="c6c48-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6c48-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c6c48-122">-Name</span></span>
<span data-ttu-id="c6c48-123">Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="c6c48-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6c48-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6c48-124">-PassThru</span></span>
<span data-ttu-id="c6c48-125">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="c6c48-125">returns true if successful</span></span>

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

### <span data-ttu-id="c6c48-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6c48-126">-ResourceGroupName</span></span>
<span data-ttu-id="c6c48-127">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="c6c48-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6c48-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6c48-128">-ResourceId</span></span>
<span data-ttu-id="c6c48-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6c48-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="c6c48-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c6c48-130">-Confirm</span></span>
<span data-ttu-id="c6c48-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c6c48-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6c48-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6c48-132">-WhatIf</span></span>
<span data-ttu-id="c6c48-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c6c48-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6c48-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c6c48-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6c48-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6c48-135">CommonParameters</span></span>
<span data-ttu-id="c6c48-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c6c48-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6c48-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c6c48-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6c48-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6c48-138">INPUTS</span></span>

### <span data-ttu-id="c6c48-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c6c48-139">System.String</span></span>

### <span data-ttu-id="c6c48-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="c6c48-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="c6c48-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6c48-141">OUTPUTS</span></span>

### <span data-ttu-id="c6c48-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="c6c48-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="c6c48-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c6c48-143">NOTES</span></span>

## <span data-ttu-id="c6c48-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6c48-144">RELATED LINKS</span></span>
