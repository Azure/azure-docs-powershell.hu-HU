---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 30D56D40-2EA0-48D1-846A-AFB4A987E08F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9dac9858a251e0390fd2a11a2c01dddede1613b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015754"
---
# <span data-ttu-id="6eff9-101">Set-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="6eff9-101">Set-AzureSiteRecoveryVM</span></span>

## <span data-ttu-id="6eff9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6eff9-102">SYNOPSIS</span></span>
<span data-ttu-id="6eff9-103">Egy webhely-helyreállítási védelmi entitás helyreállítási lehetőségeinek beállítása.</span><span class="sxs-lookup"><span data-stu-id="6eff9-103">Sets the recovery-side options for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="6eff9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6eff9-104">SYNTAX</span></span>

```
Set-AzureSiteRecoveryVM -VirtualMachine <ASRVirtualMachine> [-Name <String>] [-Size <String>]
 [-PrimaryNic <String>] [-RecoveryNetworkId <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6eff9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6eff9-105">DESCRIPTION</span></span>
<span data-ttu-id="6eff9-106">A **set-AzureSiteRecoveryVM** parancsmag az Azure webhely-helyreállítási védelem entitásai számára beállítja a helyreállítási terület helyreállítási beállításait, például a helyreállítási virtuális gép mérete és a helyreállítási virtuális gép hálózatát.</span><span class="sxs-lookup"><span data-stu-id="6eff9-106">The **Set-AzureSiteRecoveryVM** cmdlet sets the recovery-side protection options, such as the recovery virtual machine size and recovery virtual machine network, for Azure Site Recovery protection entities.</span></span>

## <span data-ttu-id="6eff9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6eff9-107">EXAMPLES</span></span>

### <span data-ttu-id="6eff9-108">1. példa: a frissítés engedélyezése védett virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="6eff9-108">Example 1: Allow the update on a protected virtual machine</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $VirtualMachines = Get-AzureSiteRecoveryVM -ProtectionContainer $ProtectionContainer 
PS C:\> Set-AzureSiteRecoveryVM -VirtualMachine $VirtualMachines[0] -Name "NewVirtualMachine05"
Name             : 
ID               : 8170d274-1e48-404a-b080-172ada140bc3
ClientRequestId  : 09354052-8430-4fa8-9a35-63196dd4b2b4-2015-02-03 04:19:06Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="6eff9-109">Az első parancs a **Get-AzureSiteRecoveryProtectionContainer** parancsmagot használja a védett tároló beszerzéséhez, majd a $ProtectionContainer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="6eff9-109">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="6eff9-110">A második parancs a **Get-AzureSiteRecoveryVM** parancsmag használatával kapja meg az $ProtectionContainer virtuális gépeket, majd a $VitrualMachines változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="6eff9-110">The second command gets the virtual machines in $ProtectionContainer, by using the **Get-AzureSiteRecoveryVM** cmdlet, and then stores them in the $VitrualMachines variable.</span></span>

<span data-ttu-id="6eff9-111">A végleges parancs lehetővé teszi az első virtuális gép frissítését a NewVirtualMachine05 nevű $VitrualMachines tömbben.</span><span class="sxs-lookup"><span data-stu-id="6eff9-111">The final command allows updates for the first virtual machine in the $VitrualMachines array, named NewVirtualMachine05.</span></span>

## <span data-ttu-id="6eff9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6eff9-112">PARAMETERS</span></span>

### <span data-ttu-id="6eff9-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6eff9-113">-Name</span></span>
<span data-ttu-id="6eff9-114">A cél virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6eff9-114">Specifies the name of the target virtual machine.</span></span>

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

### <span data-ttu-id="6eff9-115">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="6eff9-115">-PrimaryNic</span></span>
<span data-ttu-id="6eff9-116">Az elsődleges hálózati adapter kártyáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6eff9-116">Specifies the primary network adapter card.</span></span>

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

### <span data-ttu-id="6eff9-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="6eff9-117">-Profile</span></span>
<span data-ttu-id="6eff9-118">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="6eff9-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6eff9-119">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="6eff9-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eff9-120">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="6eff9-120">-RecoveryNetworkId</span></span>
<span data-ttu-id="6eff9-121">A helyreállítási hálózat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6eff9-121">Specifies the recovery network ID.</span></span>

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

### <span data-ttu-id="6eff9-122">-Méret</span><span class="sxs-lookup"><span data-stu-id="6eff9-122">-Size</span></span>
<span data-ttu-id="6eff9-123">A cél virtuális gép méretének meghatározása</span><span class="sxs-lookup"><span data-stu-id="6eff9-123">Specifies the target virtual machine size.</span></span>

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

### <span data-ttu-id="6eff9-124">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6eff9-124">-VirtualMachine</span></span>
<span data-ttu-id="6eff9-125">A site Recovery Virtual Machine objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6eff9-125">Specifies the Site Recovery virtual machine object.</span></span>

```yaml
Type: ASRVirtualMachine
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eff9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eff9-126">CommonParameters</span></span>
<span data-ttu-id="6eff9-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6eff9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eff9-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6eff9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eff9-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6eff9-129">INPUTS</span></span>

## <span data-ttu-id="6eff9-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6eff9-130">OUTPUTS</span></span>

## <span data-ttu-id="6eff9-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6eff9-131">NOTES</span></span>

## <span data-ttu-id="6eff9-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6eff9-132">RELATED LINKS</span></span>

[<span data-ttu-id="6eff9-133">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="6eff9-133">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="6eff9-134">Get-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="6eff9-134">Get-AzureSiteRecoveryVM</span></span>](./Get-AzureSiteRecoveryVM.md)


