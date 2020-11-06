---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 483D4C1A-D34E-40ED-B92B-82187FF321F7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/set-azurermsiterecoveryvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: b330cb59281a3f140ba30f10f31ecb5bf3b49f97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502351"
---
# <span data-ttu-id="60673-101">Set-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="60673-101">Set-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="60673-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="60673-102">SYNOPSIS</span></span>
<span data-ttu-id="60673-103">Egy webhely-helyreállítási védelmi entitás helyreállítási lehetőségeinek beállítása.</span><span class="sxs-lookup"><span data-stu-id="60673-103">Sets the recovery-side options for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60673-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="60673-104">SYNTAX</span></span>

```
Set-AzureRmSiteRecoveryVM -VirtualMachine <ASRVirtualMachine> [-Name <String>] [-Size <String>]
 [-PrimaryNic <String>] [-RecoveryNetworkId <String>] [-RecoveryNicSubnetName <String>]
 [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="60673-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="60673-105">DESCRIPTION</span></span>
<span data-ttu-id="60673-106">A **set-AzureRmSiteRecoveryVM** parancsmag az Azure webhely-helyreállítási védelem entitásai számára beállítja a helyreállítási terület helyreállítási beállításait, például a helyreállítási virtuális gép mérete és a helyreállítási virtuális gép hálózatát.</span><span class="sxs-lookup"><span data-stu-id="60673-106">The **Set-AzureRmSiteRecoveryVM** cmdlet sets the recovery-side protection options, such as the recovery virtual machine size and recovery virtual machine network, for Azure Site Recovery protection entities.</span></span>

## <span data-ttu-id="60673-107">Példák</span><span class="sxs-lookup"><span data-stu-id="60673-107">EXAMPLES</span></span>

## <span data-ttu-id="60673-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="60673-108">PARAMETERS</span></span>

### <span data-ttu-id="60673-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60673-109">-DefaultProfile</span></span>
<span data-ttu-id="60673-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="60673-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60673-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="60673-111">-Name</span></span>
<span data-ttu-id="60673-112">A cél virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="60673-112">Specifies the name of the target virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60673-113">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="60673-113">-NicSelectionType</span></span>
<span data-ttu-id="60673-114">A hálózati adapter kijelölésének tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="60673-114">Specifies the network adapter selection properties.</span></span>
<span data-ttu-id="60673-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="60673-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="60673-116">NotSelected</span><span class="sxs-lookup"><span data-stu-id="60673-116">NotSelected</span></span>
- <span data-ttu-id="60673-117">SelectedByUser</span><span class="sxs-lookup"><span data-stu-id="60673-117">SelectedByUser</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60673-118">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="60673-118">-PrimaryNic</span></span>
<span data-ttu-id="60673-119">Az elsődleges hálózati adapter kártyáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="60673-119">Specifies the primary network adapter card.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60673-120">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="60673-120">-RecoveryNetworkId</span></span>
<span data-ttu-id="60673-121">A helyreállítási hálózat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="60673-121">Specifies the recovery network ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60673-122">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="60673-122">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="60673-123">Az elsődleges hálózati adapter-vezérlő helyreállítási rendszeréhez hozzárendelt statikus IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="60673-123">Specifies the static IP address that is assigned to primary network adapter controller on recovery.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60673-124">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="60673-124">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="60673-125">Annak az Azure virtuális hálózati alhálózatnak a neve, amelyhez az elsődleges hálózati adapter vezérlőt kell csatlakoztatni a helyreállításhoz.</span><span class="sxs-lookup"><span data-stu-id="60673-125">Specifies the Azure virtual network subnet name with which to attach the primary network adapter controller on recovery.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60673-126">-Méret</span><span class="sxs-lookup"><span data-stu-id="60673-126">-Size</span></span>
<span data-ttu-id="60673-127">A cél virtuális gép méretének meghatározása</span><span class="sxs-lookup"><span data-stu-id="60673-127">Specifies the target virtual machine size.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60673-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="60673-128">-VirtualMachine</span></span>
<span data-ttu-id="60673-129">A site Recovery Virtual Machine objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="60673-129">Specifies the Site Recovery virtual machine object.</span></span>

```yaml
Type: ASRVirtualMachine
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60673-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60673-130">CommonParameters</span></span>
<span data-ttu-id="60673-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="60673-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60673-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60673-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60673-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="60673-133">INPUTS</span></span>

### <span data-ttu-id="60673-134">ASRVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="60673-134">ASRVirtualMachine</span></span>
<span data-ttu-id="60673-135">A ' VirtualMachine ' paraméter az "ASRVirtualMachine" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="60673-135">Parameter 'VirtualMachine' accepts value of type 'ASRVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="60673-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60673-136">OUTPUTS</span></span>

### <span data-ttu-id="60673-137">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="60673-137">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="60673-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="60673-138">NOTES</span></span>

## <span data-ttu-id="60673-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60673-139">RELATED LINKS</span></span>

[<span data-ttu-id="60673-140">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="60673-140">Get-AzureRmSiteRecoveryVM</span></span>](./Get-AzureRmSiteRecoveryVM.md)
