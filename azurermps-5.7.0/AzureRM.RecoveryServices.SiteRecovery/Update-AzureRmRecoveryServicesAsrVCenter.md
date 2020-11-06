---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 298443c4b962a2be6c5cf3849657d0fe8bbaf978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493032"
---
# <span data-ttu-id="9a02e-101">Update-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="9a02e-101">Update-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="9a02e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9a02e-102">SYNOPSIS</span></span>
<span data-ttu-id="9a02e-103">A regisztrált vCenter vonatkozó feltárási adatok frissítése.</span><span class="sxs-lookup"><span data-stu-id="9a02e-103">Update discovery details for a registered vCenter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a02e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9a02e-104">SYNTAX</span></span>

### <span data-ttu-id="9a02e-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9a02e-105">Default (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a02e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9a02e-106">ByResourceId</span></span>
```
Update-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a02e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9a02e-107">DESCRIPTION</span></span>
<span data-ttu-id="9a02e-108">Az **Update-AzureRmRecoveryServicesAsrvCenter** parancsmag frissíti egy regisztrált vCenter felderítési adatait.</span><span class="sxs-lookup"><span data-stu-id="9a02e-108">The **Update-AzureRmRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="9a02e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9a02e-109">EXAMPLES</span></span>

### <span data-ttu-id="9a02e-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9a02e-110">Example 1</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="9a02e-111">A regisztrált vCenter vonatkozó feltárási adatok frissítése.</span><span class="sxs-lookup"><span data-stu-id="9a02e-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="9a02e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9a02e-112">PARAMETERS</span></span>

### <span data-ttu-id="9a02e-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="9a02e-113">-Account</span></span>
<span data-ttu-id="9a02e-114">bejelentkezési hitelesítő adatok vCenter-fiókja.</span><span class="sxs-lookup"><span data-stu-id="9a02e-114">vCenter login credentials account.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a02e-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9a02e-115">-Confirm</span></span>
<span data-ttu-id="9a02e-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9a02e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a02e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a02e-117">-DefaultProfile</span></span>
<span data-ttu-id="9a02e-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a02e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a02e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a02e-119">-InputObject</span></span>
<span data-ttu-id="9a02e-120">A vCenter Server objektum a feltárási adatok frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="9a02e-120">The vCenter server object to update discovery details for.</span></span>

```yaml
Type: ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a02e-121">-Port</span><span class="sxs-lookup"><span data-stu-id="9a02e-121">-Port</span></span>
<span data-ttu-id="9a02e-122">A vCenter-kiszolgáló TCP-portja, amelyet a felderítéshez szeretne használni.</span><span class="sxs-lookup"><span data-stu-id="9a02e-122">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: Int32
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a02e-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a02e-123">-ResourceId</span></span>
<span data-ttu-id="9a02e-124">A vCenter resourceId adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a02e-124">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a02e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a02e-125">-WhatIf</span></span>
<span data-ttu-id="9a02e-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9a02e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a02e-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9a02e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a02e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a02e-128">CommonParameters</span></span>
<span data-ttu-id="9a02e-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9a02e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a02e-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a02e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a02e-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a02e-131">INPUTS</span></span>

### <span data-ttu-id="9a02e-132">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="9a02e-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="9a02e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a02e-133">OUTPUTS</span></span>

### <span data-ttu-id="9a02e-134">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 0.1.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9a02e-134">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9a02e-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9a02e-135">NOTES</span></span>

## <span data-ttu-id="9a02e-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a02e-136">RELATED LINKS</span></span>
