---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
ms.openlocfilehash: ec8703b5b107758a331407d431f871acf249885d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013903"
---
# <span data-ttu-id="a33e9-101">Remove-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="a33e9-101">Remove-AzStackEdgeUser</span></span>

## <span data-ttu-id="a33e9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a33e9-102">SYNOPSIS</span></span>
<span data-ttu-id="a33e9-103">Eltávolít egy felhasználót egy eszközön.</span><span class="sxs-lookup"><span data-stu-id="a33e9-103">Removes a user on a device.</span></span>

## <span data-ttu-id="a33e9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a33e9-104">SYNTAX</span></span>

### <span data-ttu-id="a33e9-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a33e9-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a33e9-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a33e9-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a33e9-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a33e9-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeUser [-InputObject] <PSStackEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a33e9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a33e9-108">DESCRIPTION</span></span>
<span data-ttu-id="a33e9-109">A **Remove-AzStackEdgeUser** parancsmag eltávolítja a felhasználót a halom szélén lévő eszközön.</span><span class="sxs-lookup"><span data-stu-id="a33e9-109">The **Remove-AzStackEdgeUser** cmdlet removes a user on the Stack Edge device.</span></span> <span data-ttu-id="a33e9-110">Csak a típusú felhasználók létrehozása `Share` támogatott.</span><span class="sxs-lookup"><span data-stu-id="a33e9-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="a33e9-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a33e9-111">EXAMPLES</span></span>

### <span data-ttu-id="a33e9-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a33e9-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="a33e9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a33e9-113">PARAMETERS</span></span>

### <span data-ttu-id="a33e9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a33e9-114">-AsJob</span></span>
<span data-ttu-id="a33e9-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a33e9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a33e9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a33e9-116">-DefaultProfile</span></span>
<span data-ttu-id="a33e9-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a33e9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a33e9-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a33e9-118">-DeviceName</span></span>
<span data-ttu-id="a33e9-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="a33e9-119">Device Name</span></span>

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

### <span data-ttu-id="a33e9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a33e9-120">-InputObject</span></span>
<span data-ttu-id="a33e9-121">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="a33e9-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: User

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a33e9-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a33e9-122">-Name</span></span>
<span data-ttu-id="a33e9-123">Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="a33e9-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a33e9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a33e9-124">-PassThru</span></span>
<span data-ttu-id="a33e9-125">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="a33e9-125">returns true if successful</span></span>

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

### <span data-ttu-id="a33e9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a33e9-126">-ResourceGroupName</span></span>
<span data-ttu-id="a33e9-127">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="a33e9-127">Resource Group Name</span></span>

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

### <span data-ttu-id="a33e9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a33e9-128">-ResourceId</span></span>
<span data-ttu-id="a33e9-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a33e9-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="a33e9-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a33e9-130">-Confirm</span></span>
<span data-ttu-id="a33e9-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a33e9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a33e9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a33e9-132">-WhatIf</span></span>
<span data-ttu-id="a33e9-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a33e9-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a33e9-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a33e9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a33e9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a33e9-135">CommonParameters</span></span>
<span data-ttu-id="a33e9-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a33e9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a33e9-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a33e9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a33e9-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a33e9-138">INPUTS</span></span>

### <span data-ttu-id="a33e9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a33e9-139">System.String</span></span>

### <span data-ttu-id="a33e9-140">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="a33e9-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="a33e9-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a33e9-141">OUTPUTS</span></span>

### <span data-ttu-id="a33e9-142">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a33e9-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="a33e9-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a33e9-143">NOTES</span></span>

## <span data-ttu-id="a33e9-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a33e9-144">RELATED LINKS</span></span>
