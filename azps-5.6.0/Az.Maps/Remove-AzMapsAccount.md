---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/powershell/module/az.maps/remove-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
ms.openlocfilehash: e14e080ab04c3fc9cb191c240e3d71c00cc1c7f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006645"
---
# <span data-ttu-id="2f5a8-101">Remove-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="2f5a8-101">Remove-AzMapsAccount</span></span>

## <span data-ttu-id="2f5a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f5a8-102">SYNOPSIS</span></span>
<span data-ttu-id="2f5a8-103">Töröl egy Azure Maps-fiókot.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-103">Deletes an Azure Maps account.</span></span>

## <span data-ttu-id="2f5a8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2f5a8-104">SYNTAX</span></span>

### <span data-ttu-id="2f5a8-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f5a8-105">NameParameterSet (Default)</span></span>
```
Remove-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f5a8-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f5a8-106">InputObjectParameterSet</span></span>
```
Remove-AzMapsAccount [-InputObject <PSMapsAccount>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f5a8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f5a8-107">ResourceIdParameterSet</span></span>
```
Remove-AzMapsAccount [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f5a8-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2f5a8-108">DESCRIPTION</span></span>
<span data-ttu-id="2f5a8-109">A Remove-AzMapsAccount parancsmag törli a megadott Azure Maps-fiókot.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-109">The Remove-AzMapsAccount cmdlet deletes the specified Azure Maps account.</span></span>

## <span data-ttu-id="2f5a8-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2f5a8-110">EXAMPLES</span></span>

### <span data-ttu-id="2f5a8-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="2f5a8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="2f5a8-112">Törli a MyAccount fiókot a MyResourceGroup erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="2f5a8-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="2f5a8-113">Example 2</span></span>
```
PS C:\> Remove-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="2f5a8-114">A megadott Azure Maps-fiók törlése.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-114">Deletes the specified Azure Maps Account.</span></span>

## <span data-ttu-id="2f5a8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f5a8-115">PARAMETERS</span></span>

### <span data-ttu-id="2f5a8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f5a8-116">-DefaultProfile</span></span>
<span data-ttu-id="2f5a8-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f5a8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f5a8-118">-InputObject</span></span>
<span data-ttu-id="2f5a8-119">Térképek-fiók, amely a Get-AzMapsAccount fájlból van be van pávava.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-119">Maps Account piped from Get-AzMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f5a8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2f5a8-120">-Name</span></span>
<span data-ttu-id="2f5a8-121">Térképek-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-121">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f5a8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f5a8-122">-PassThru</span></span>
<span data-ttu-id="2f5a8-123">Adja vissza, hogy a megadott fiók törlése sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-123">Return whether the specified account was successfully deleted or not.</span></span>

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

### <span data-ttu-id="2f5a8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f5a8-124">-ResourceGroupName</span></span>
<span data-ttu-id="2f5a8-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f5a8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f5a8-126">-ResourceId</span></span>
<span data-ttu-id="2f5a8-127">Leképezi a Fiók erőforrásazonosítóját.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f5a8-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f5a8-128">-Confirm</span></span>
<span data-ttu-id="2f5a8-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f5a8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f5a8-130">-WhatIf</span></span>
<span data-ttu-id="2f5a8-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f5a8-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f5a8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f5a8-133">CommonParameters</span></span>
<span data-ttu-id="2f5a8-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f5a8-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f5a8-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f5a8-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2f5a8-136">INPUTS</span></span>

### <span data-ttu-id="2f5a8-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2f5a8-137">System.String</span></span>

### <span data-ttu-id="2f5a8-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="2f5a8-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="2f5a8-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f5a8-139">OUTPUTS</span></span>

### <span data-ttu-id="2f5a8-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2f5a8-140">System.Boolean</span></span>

## <span data-ttu-id="2f5a8-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2f5a8-141">NOTES</span></span>

## <span data-ttu-id="2f5a8-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f5a8-142">RELATED LINKS</span></span>
