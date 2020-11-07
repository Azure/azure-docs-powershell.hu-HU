---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: d6e26eb293a2b87fccc0749b6d5c53d15d7d860f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838999"
---
# <span data-ttu-id="90a45-101">Update-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="90a45-101">Update-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="90a45-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="90a45-102">SYNOPSIS</span></span>
<span data-ttu-id="90a45-103">A regisztrált vCenter vonatkozó feltárási adatok frissítése.</span><span class="sxs-lookup"><span data-stu-id="90a45-103">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="90a45-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="90a45-104">SYNTAX</span></span>

### <span data-ttu-id="90a45-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="90a45-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90a45-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="90a45-106">ByResourceId</span></span>
```
Update-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90a45-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="90a45-107">DESCRIPTION</span></span>
<span data-ttu-id="90a45-108">Az **Update-AzRecoveryServicesAsrvCenter** parancsmag frissíti egy regisztrált vCenter felderítési adatait.</span><span class="sxs-lookup"><span data-stu-id="90a45-108">The **Update-AzRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="90a45-109">Példák</span><span class="sxs-lookup"><span data-stu-id="90a45-109">EXAMPLES</span></span>

### <span data-ttu-id="90a45-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="90a45-110">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="90a45-111">A regisztrált vCenter vonatkozó feltárási adatok frissítése.</span><span class="sxs-lookup"><span data-stu-id="90a45-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="90a45-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="90a45-112">PARAMETERS</span></span>

### <span data-ttu-id="90a45-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="90a45-113">-Account</span></span>
<span data-ttu-id="90a45-114">bejelentkezési hitelesítő adatok vCenter-fiókja.</span><span class="sxs-lookup"><span data-stu-id="90a45-114">vCenter login credentials account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90a45-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90a45-115">-DefaultProfile</span></span>
<span data-ttu-id="90a45-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="90a45-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90a45-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90a45-117">-InputObject</span></span>
<span data-ttu-id="90a45-118">A vCenter Server objektum a feltárási adatok frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="90a45-118">The vCenter server object to update discovery details for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90a45-119">-Port</span><span class="sxs-lookup"><span data-stu-id="90a45-119">-Port</span></span>
<span data-ttu-id="90a45-120">A vCenter-kiszolgáló TCP-portja, amelyet a felderítéshez szeretne használni.</span><span class="sxs-lookup"><span data-stu-id="90a45-120">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90a45-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90a45-121">-ResourceId</span></span>
<span data-ttu-id="90a45-122">A vCenter resourceId adja meg.</span><span class="sxs-lookup"><span data-stu-id="90a45-122">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90a45-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="90a45-123">-Confirm</span></span>
<span data-ttu-id="90a45-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="90a45-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90a45-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90a45-125">-WhatIf</span></span>
<span data-ttu-id="90a45-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="90a45-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90a45-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="90a45-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90a45-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90a45-128">CommonParameters</span></span>
<span data-ttu-id="90a45-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="90a45-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90a45-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90a45-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90a45-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="90a45-131">INPUTS</span></span>

### <span data-ttu-id="90a45-132">System. String</span><span class="sxs-lookup"><span data-stu-id="90a45-132">System.String</span></span>

### <span data-ttu-id="90a45-133">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="90a45-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="90a45-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90a45-134">OUTPUTS</span></span>

### <span data-ttu-id="90a45-135">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="90a45-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="90a45-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="90a45-136">NOTES</span></span>

## <span data-ttu-id="90a45-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90a45-137">RELATED LINKS</span></span>
