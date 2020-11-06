---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: be521545111667493c5b0e268013ffa4464ed3a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492214"
---
# <span data-ttu-id="2db76-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="2db76-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="2db76-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2db76-102">SYNOPSIS</span></span>
<span data-ttu-id="2db76-103">Frissíti a megadott Azure-webhely-helyreállítási hálózati megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="2db76-103">Updates the specified azure site recovery network mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2db76-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2db76-104">SYNTAX</span></span>

### <span data-ttu-id="2db76-105">ByNetworkObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2db76-105">ByNetworkObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2db76-106">ById</span><span class="sxs-lookup"><span data-stu-id="2db76-106">ById</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2db76-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2db76-107">DESCRIPTION</span></span>
<span data-ttu-id="2db76-108">Az **Update-AzureRmRecoveryServicesAsrNetworkMapping** parancsmag frissíti a megadott Azure-webhely-helyreállítási hálózati megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="2db76-108">The **Update-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="2db76-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2db76-109">EXAMPLES</span></span>

### <span data-ttu-id="2db76-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2db76-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="2db76-111">Elindítja a hálózati megfeleltetési műveletet a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="2db76-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="2db76-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2db76-112">PARAMETERS</span></span>

### <span data-ttu-id="2db76-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2db76-113">-Confirm</span></span>
<span data-ttu-id="2db76-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2db76-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2db76-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2db76-115">-DefaultProfile</span></span>
<span data-ttu-id="2db76-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2db76-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="2db76-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2db76-117">-InputObject</span></span>
<span data-ttu-id="2db76-118">Beviteli objektum: Itt adhatja meg, hogy az ASR-hálózati megfeleltetési objektum az ASR-hálózati megfeleltetésnek megfelelően frissüljön-e.</span><span class="sxs-lookup"><span data-stu-id="2db76-118">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2db76-119">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="2db76-119">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="2db76-120">A helyreállítási Azure hálózati AZONOSÍTÓját adja meg a hálózati megfeleltetéshez.</span><span class="sxs-lookup"><span data-stu-id="2db76-120">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2db76-121">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="2db76-121">-RecoveryNetwork</span></span>
<span data-ttu-id="2db76-122">A hálózati megfeleltetéshez a helyreállítási hálózat objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2db76-122">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2db76-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2db76-123">-WhatIf</span></span>
<span data-ttu-id="2db76-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2db76-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2db76-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2db76-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2db76-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2db76-126">CommonParameters</span></span>
<span data-ttu-id="2db76-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2db76-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2db76-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2db76-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2db76-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2db76-129">INPUTS</span></span>

### <span data-ttu-id="2db76-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="2db76-130">None</span></span>

## <span data-ttu-id="2db76-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2db76-131">OUTPUTS</span></span>

### <span data-ttu-id="2db76-132">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2db76-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2db76-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2db76-133">NOTES</span></span>

## <span data-ttu-id="2db76-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2db76-134">RELATED LINKS</span></span>
