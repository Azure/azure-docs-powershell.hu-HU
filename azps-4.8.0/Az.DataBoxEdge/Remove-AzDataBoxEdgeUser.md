---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
ms.openlocfilehash: cecfa3e009f6d6fbc7167c4b8f1ca110d547b5b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182340"
---
# <span data-ttu-id="1846b-101">Remove-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="1846b-101">Remove-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="1846b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1846b-102">SYNOPSIS</span></span>
<span data-ttu-id="1846b-103">Eltávolít egy felhasználót egy eszközön.</span><span class="sxs-lookup"><span data-stu-id="1846b-103">Removes a user on a device.</span></span>

## <span data-ttu-id="1846b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1846b-104">SYNTAX</span></span>

### <span data-ttu-id="1846b-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1846b-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1846b-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1846b-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1846b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1846b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-InputObject] <PSDataBoxEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1846b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1846b-108">DESCRIPTION</span></span>
<span data-ttu-id="1846b-109">A **Remove-AzDataBoxEdgeUser** parancsmag eltávolítja a felhasználót az adatmező szélén lévő eszközön.</span><span class="sxs-lookup"><span data-stu-id="1846b-109">The **Remove-AzDataBoxEdgeUser** cmdlet removes a user on the Data Box Edge device.</span></span> <span data-ttu-id="1846b-110">Csak a típusú felhasználók létrehozása `Share` támogatott.</span><span class="sxs-lookup"><span data-stu-id="1846b-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="1846b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="1846b-111">EXAMPLES</span></span>

### <span data-ttu-id="1846b-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1846b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="1846b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1846b-113">PARAMETERS</span></span>

### <span data-ttu-id="1846b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1846b-114">-AsJob</span></span>
<span data-ttu-id="1846b-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1846b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1846b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1846b-116">-DefaultProfile</span></span>
<span data-ttu-id="1846b-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1846b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1846b-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="1846b-118">-DeviceName</span></span>
<span data-ttu-id="1846b-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="1846b-119">Device Name</span></span>

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

### <span data-ttu-id="1846b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1846b-120">-InputObject</span></span>
<span data-ttu-id="1846b-121">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="1846b-121">Input Object</span></span>

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

### <span data-ttu-id="1846b-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1846b-122">-Name</span></span>
<span data-ttu-id="1846b-123">Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="1846b-123">Username</span></span>

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

### <span data-ttu-id="1846b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1846b-124">-PassThru</span></span>
<span data-ttu-id="1846b-125">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="1846b-125">returns true if successful</span></span>

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

### <span data-ttu-id="1846b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1846b-126">-ResourceGroupName</span></span>
<span data-ttu-id="1846b-127">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="1846b-127">Resource Group Name</span></span>

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

### <span data-ttu-id="1846b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1846b-128">-ResourceId</span></span>
<span data-ttu-id="1846b-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="1846b-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="1846b-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1846b-130">-Confirm</span></span>
<span data-ttu-id="1846b-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1846b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1846b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1846b-132">-WhatIf</span></span>
<span data-ttu-id="1846b-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1846b-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1846b-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1846b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1846b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1846b-135">CommonParameters</span></span>
<span data-ttu-id="1846b-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1846b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1846b-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1846b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1846b-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1846b-138">INPUTS</span></span>

### <span data-ttu-id="1846b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1846b-139">System.String</span></span>

### <span data-ttu-id="1846b-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="1846b-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="1846b-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1846b-141">OUTPUTS</span></span>

### <span data-ttu-id="1846b-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="1846b-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="1846b-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1846b-143">NOTES</span></span>

## <span data-ttu-id="1846b-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1846b-144">RELATED LINKS</span></span>
