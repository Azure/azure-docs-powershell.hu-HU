---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/remove-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
ms.openlocfilehash: b84a5d6cbbf090243a63ad9919a3fbb1977d77f5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010906"
---
# <span data-ttu-id="b1cac-101">Remove-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="b1cac-101">Remove-AzMapsAccount</span></span>

## <span data-ttu-id="b1cac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b1cac-102">SYNOPSIS</span></span>
<span data-ttu-id="b1cac-103">Azure Maps-fiók törlése</span><span class="sxs-lookup"><span data-stu-id="b1cac-103">Deletes an Azure Maps account.</span></span>

## <span data-ttu-id="b1cac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b1cac-104">SYNTAX</span></span>

### <span data-ttu-id="b1cac-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b1cac-105">NameParameterSet (Default)</span></span>
```
Remove-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1cac-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1cac-106">InputObjectParameterSet</span></span>
```
Remove-AzMapsAccount [-InputObject <PSMapsAccount>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1cac-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1cac-107">ResourceIdParameterSet</span></span>
```
Remove-AzMapsAccount [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1cac-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b1cac-108">DESCRIPTION</span></span>
<span data-ttu-id="b1cac-109">A Remove-AzMapsAccount parancsmag törli a megadott Azure Maps-fiókot.</span><span class="sxs-lookup"><span data-stu-id="b1cac-109">The Remove-AzMapsAccount cmdlet deletes the specified Azure Maps account.</span></span>

## <span data-ttu-id="b1cac-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b1cac-110">EXAMPLES</span></span>

### <span data-ttu-id="b1cac-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b1cac-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="b1cac-112">Törli a fiók MyAccount az erőforrás csoport MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b1cac-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="b1cac-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="b1cac-113">Example 2</span></span>
```
PS C:\> Remove-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="b1cac-114">Törli a megadott Azure Maps-fiókot.</span><span class="sxs-lookup"><span data-stu-id="b1cac-114">Deletes the specified Azure Maps Account.</span></span>

## <span data-ttu-id="b1cac-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b1cac-115">PARAMETERS</span></span>

### <span data-ttu-id="b1cac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1cac-116">-DefaultProfile</span></span>
<span data-ttu-id="b1cac-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b1cac-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1cac-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1cac-118">-InputObject</span></span>
<span data-ttu-id="b1cac-119">A Get-AzMapsAccount átirányítja a fiókját.</span><span class="sxs-lookup"><span data-stu-id="b1cac-119">Maps Account piped from Get-AzMapsAccount.</span></span>

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

### <span data-ttu-id="b1cac-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b1cac-120">-Name</span></span>
<span data-ttu-id="b1cac-121">A fiók nevének megfeleltetése</span><span class="sxs-lookup"><span data-stu-id="b1cac-121">Maps Account Name.</span></span>

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

### <span data-ttu-id="b1cac-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1cac-122">-PassThru</span></span>
<span data-ttu-id="b1cac-123">A megadott fiók sikeres törlésének visszaadása.</span><span class="sxs-lookup"><span data-stu-id="b1cac-123">Return whether the specified account was successfully deleted or not.</span></span>

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

### <span data-ttu-id="b1cac-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1cac-124">-ResourceGroupName</span></span>
<span data-ttu-id="b1cac-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="b1cac-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="b1cac-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1cac-126">-ResourceId</span></span>
<span data-ttu-id="b1cac-127">Térképek fiók ResourceId.</span><span class="sxs-lookup"><span data-stu-id="b1cac-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="b1cac-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b1cac-128">-Confirm</span></span>
<span data-ttu-id="b1cac-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b1cac-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1cac-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1cac-130">-WhatIf</span></span>
<span data-ttu-id="b1cac-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b1cac-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1cac-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b1cac-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1cac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1cac-133">CommonParameters</span></span>
<span data-ttu-id="b1cac-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b1cac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1cac-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1cac-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1cac-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1cac-136">INPUTS</span></span>

### <span data-ttu-id="b1cac-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b1cac-137">System.String</span></span>

### <span data-ttu-id="b1cac-138">Microsoft. Azure. commands. maps. models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="b1cac-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="b1cac-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1cac-139">OUTPUTS</span></span>

### <span data-ttu-id="b1cac-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b1cac-140">System.Boolean</span></span>

## <span data-ttu-id="b1cac-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b1cac-141">NOTES</span></span>

## <span data-ttu-id="b1cac-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1cac-142">RELATED LINKS</span></span>
