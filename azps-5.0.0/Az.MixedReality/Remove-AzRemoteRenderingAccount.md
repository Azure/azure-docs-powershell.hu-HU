---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
ms.openlocfilehash: bfcbaa723dc2d06d74ba4d515affd2f19a51ec3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187300"
---
# <span data-ttu-id="5b376-101">Remove-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="5b376-101">Remove-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="5b376-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5b376-102">SYNOPSIS</span></span>
<span data-ttu-id="5b376-103">Távoli megjelenítési fiók törlése</span><span class="sxs-lookup"><span data-stu-id="5b376-103">Delete Remote Rendering Account</span></span>

## <span data-ttu-id="5b376-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5b376-104">SYNTAX</span></span>

### <span data-ttu-id="5b376-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5b376-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b376-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b376-106">ResourceIdParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b376-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b376-107">PipelineParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -InputObject <PSRemoteRenderingAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b376-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5b376-108">DESCRIPTION</span></span>
<span data-ttu-id="5b376-109">Meghatározott távoli megjelenítési fiók törlése bizonyos előfizetésből és erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="5b376-109">Delete specified Remote Rendering Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="5b376-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5b376-110">EXAMPLES</span></span>

### <span data-ttu-id="5b376-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5b376-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="5b376-112">A "példa" távoli megjelenítési fiók törlése a jelenlegi előfizetésből és erőforráscsoporthoz "rg1".</span><span class="sxs-lookup"><span data-stu-id="5b376-112">Delete Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="5b376-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5b376-113">PARAMETERS</span></span>

### <span data-ttu-id="5b376-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5b376-114">-Confirm</span></span>
<span data-ttu-id="5b376-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5b376-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b376-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b376-116">-DefaultProfile</span></span>
<span data-ttu-id="5b376-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5b376-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b376-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b376-118">-InputObject</span></span>
<span data-ttu-id="5b376-119">Az egyéni tartomány-objektum.</span><span class="sxs-lookup"><span data-stu-id="5b376-119">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b376-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5b376-120">-Name</span></span>
<span data-ttu-id="5b376-121">Távoli megjelenítési fiók neve.</span><span class="sxs-lookup"><span data-stu-id="5b376-121">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b376-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b376-122">-PassThru</span></span>
<span data-ttu-id="5b376-123">Ha meg van adva a visszatérési objektum</span><span class="sxs-lookup"><span data-stu-id="5b376-123">Return object if specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b376-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b376-124">-ResourceGroupName</span></span>
<span data-ttu-id="5b376-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="5b376-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b376-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b376-126">-ResourceId</span></span>
<span data-ttu-id="5b376-127">A távoli megjelenítési fiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5b376-127">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b376-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b376-128">-WhatIf</span></span>
<span data-ttu-id="5b376-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5b376-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b376-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5b376-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b376-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b376-131">CommonParameters</span></span>
<span data-ttu-id="5b376-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5b376-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5b376-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b376-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b376-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b376-134">INPUTS</span></span>

### <span data-ttu-id="5b376-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5b376-135">System.String</span></span>

### <span data-ttu-id="5b376-136">Microsoft. Azure. Command. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="5b376-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

### <span data-ttu-id="5b376-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5b376-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5b376-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b376-138">OUTPUTS</span></span>

### <span data-ttu-id="5b376-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5b376-139">System.Boolean</span></span>

## <span data-ttu-id="5b376-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5b376-140">NOTES</span></span>

## <span data-ttu-id="5b376-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b376-141">RELATED LINKS</span></span>
