---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: b3790105f2404cc7bf50ef1200ce0978e8f0b15d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501872"
---
# <span data-ttu-id="1aeb5-101">Set-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="1aeb5-101">Set-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="1aeb5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1aeb5-102">SYNOPSIS</span></span>
<span data-ttu-id="1aeb5-103">A DevTest Labs-ban egy Lab virtuális gép felhasználónként házirendet állít be.</span><span class="sxs-lookup"><span data-stu-id="1aeb5-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1aeb5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1aeb5-104">SYNTAX</span></span>

### <span data-ttu-id="1aeb5-105">Engedélyezés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1aeb5-105">Enable (Default)</span></span>
```
Set-AzureRmDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1aeb5-106">Megbénít</span><span class="sxs-lookup"><span data-stu-id="1aeb5-106">Disable</span></span>
```
Set-AzureRmDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1aeb5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1aeb5-107">DESCRIPTION</span></span>
<span data-ttu-id="1aeb5-108">A **set-AzureRmDtlVMsPerUserPolicy** parancsmag egy Lab virtuális gép felhasználónként való beállítását állítja be, amely a felhasználónként engedélyezett virtuális gépek maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1aeb5-108">The **Set-AzureRmDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="1aeb5-109">A parancsmag a megadott erőforráscsoportot és a laboratórium nevét használja a házirend beállításához.</span><span class="sxs-lookup"><span data-stu-id="1aeb5-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="1aeb5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1aeb5-110">EXAMPLES</span></span>

## <span data-ttu-id="1aeb5-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1aeb5-111">PARAMETERS</span></span>

### <span data-ttu-id="1aeb5-112">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="1aeb5-112">-Disable</span></span>
<span data-ttu-id="1aeb5-113">Jelzi, hogy ez a parancsmag letiltja a Lab házirendet.</span><span class="sxs-lookup"><span data-stu-id="1aeb5-113">Indicates that this cmdlet disables the policy for the lab.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aeb5-114">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="1aeb5-114">-Enable</span></span>
<span data-ttu-id="1aeb5-115">Azt jelzi, hogy ez a parancsmag engedélyezi a Lab házirendet.</span><span class="sxs-lookup"><span data-stu-id="1aeb5-115">Indicates that this cmdlet enables the policy for the lab.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aeb5-116">-LabName</span><span class="sxs-lookup"><span data-stu-id="1aeb5-116">-LabName</span></span>
<span data-ttu-id="1aeb5-117">Annak a laboratóriumnak a nevét adja meg, amelynek a parancsmagja a virtuális gépek felhasználónkénti házirendjének beállítása.</span><span class="sxs-lookup"><span data-stu-id="1aeb5-117">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1aeb5-118">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="1aeb5-118">-MaxVMs</span></span>
<span data-ttu-id="1aeb5-119">A laboratóriumban létrehozható virtuális gépek maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1aeb5-119">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aeb5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aeb5-120">-ResourceGroupName</span></span>
<span data-ttu-id="1aeb5-121">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="1aeb5-121">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1aeb5-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1aeb5-122">-Confirm</span></span>
<span data-ttu-id="1aeb5-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1aeb5-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aeb5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1aeb5-124">-WhatIf</span></span>
<span data-ttu-id="1aeb5-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1aeb5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1aeb5-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1aeb5-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aeb5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aeb5-127">-DefaultProfile</span></span>
<span data-ttu-id="1aeb5-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1aeb5-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aeb5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aeb5-129">CommonParameters</span></span>
<span data-ttu-id="1aeb5-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1aeb5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aeb5-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1aeb5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aeb5-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1aeb5-132">INPUTS</span></span>

## <span data-ttu-id="1aeb5-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1aeb5-133">OUTPUTS</span></span>

### <span data-ttu-id="1aeb5-134">Microsoft. Azure. Command. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="1aeb5-134">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="1aeb5-135">Ez a parancsmag azt a házirendet adja eredményül, amely megadja a laboratóriumban egy felhasználó által létrehozható virtuális gépek maximális számát.</span><span class="sxs-lookup"><span data-stu-id="1aeb5-135">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created by a user in the lab.</span></span>

## <span data-ttu-id="1aeb5-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1aeb5-136">NOTES</span></span>

## <span data-ttu-id="1aeb5-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1aeb5-137">RELATED LINKS</span></span>

[<span data-ttu-id="1aeb5-138">Get-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="1aeb5-138">Get-AzureRmDtlVMsPerUserPolicy</span></span>](./Get-AzureRmDtlVMsPerUserPolicy.md)


