---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 185506BC-6155-4517-BCBD-BCDE7450C7A8
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8017c2947a8d046226a63b5ed07b3714c35b22c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016410"
---
# <span data-ttu-id="a1eea-101">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span><span class="sxs-lookup"><span data-stu-id="a1eea-101">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span></span>

## <span data-ttu-id="a1eea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a1eea-102">SYNOPSIS</span></span>
<span data-ttu-id="a1eea-103">Disszociációs feladatot indít egy webhely-helyreállítási védelemmel ellátni kívánt replikációs házirendben.</span><span class="sxs-lookup"><span data-stu-id="a1eea-103">Starts a dissociation job on a replication policy associated with a Site Recovery protection container.</span></span>

## <span data-ttu-id="a1eea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a1eea-104">SYNTAX</span></span>

### <span data-ttu-id="a1eea-105">EnterpriseToAzure (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a1eea-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureSiteRecoveryProtectionProfileDissociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a1eea-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="a1eea-106">EnterpriseToEnterprise</span></span>
```
Start-AzureSiteRecoveryProtectionProfileDissociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a1eea-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a1eea-107">DESCRIPTION</span></span>
<span data-ttu-id="a1eea-108">A **Start-AzureSiteRecoveryProtectionProfileDissociationJob** parancsmag disszociációs feladatot kezdeményez az Azure-webhely helyreállítási védelmi tárolója által társított replikációs házirendben.</span><span class="sxs-lookup"><span data-stu-id="a1eea-108">The **Start-AzureSiteRecoveryProtectionProfileDissociationJob** cmdlet initiates a dissociation job on the replication policy associated with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="a1eea-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a1eea-109">EXAMPLES</span></span>

### <span data-ttu-id="a1eea-110">1. példa: védelmi profil szétválasztása</span><span class="sxs-lookup"><span data-stu-id="a1eea-110">Example 1: Dissociate a protection profile</span></span>
```
PS C:\> $ProtectionContainer01 = Get-AzureSiteRecoveryProtectionContainer -Id "5ba2ea95-856d-4033-9ca3-91e3e2c080b9"
PS C:\> $ProtectionContainer02 = Get-AzureSiteRecoveryProtectionContainer -Id "cf011f2a-aa19-443c-9f60-357f6b8afb77"
PS C:\> Start-AzureSiteRecoveryProtectionProfileDissociationJob -PrimaryProtectionContainer $ProtectionContainer01 -ProtectionProfile $ProtectionContainer01.AvailableProtectionProfiles[0] -RecoveryProtectionContainer $ProtectionContainer02
Name             : MyProtectionProfile
ID               : 51978b0f-9241-4153-9171-2e19344f0805
ClientRequestId  : bb6f3200-b7c6-4c6f-bcbc-a70bb9946f03-2015-01-30 02:55:55Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="a1eea-111">Az első parancs a **Get-AzureSiteRecoveryProtectionContainer** parancsmag használatával kap védelmi tárolót, és a tárolót a $ProtectionContainer 01 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a1eea-111">The first command gets a protection container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that container in the $ProtectionContainer01 variable.</span></span>

<span data-ttu-id="a1eea-112">A második parancs a védelmi tárolót kapja, majd a $ProtectionContainer 02 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a1eea-112">The second command gets a protection container, and then stores it in the $ProtectionContainer02 variable.</span></span>

<span data-ttu-id="a1eea-113">A végleges parancs elválasztja az elsődleges védelmi tárolóként az $ProtectionContainer 01-ben tárolt tároló védelmi profilját.</span><span class="sxs-lookup"><span data-stu-id="a1eea-113">The final command dissociates the protection profile from the container stored in $ProtectionContainer01 as the primary protection container.</span></span>
<span data-ttu-id="a1eea-114">A parancs elválasztja a $ProtectionContainer 02-ben tárolt tárolót a helyreállítási védelmi tárolóban.</span><span class="sxs-lookup"><span data-stu-id="a1eea-114">The command dissociates the container stored in $ProtectionContainer02 as the recovery protection container.</span></span>

## <span data-ttu-id="a1eea-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a1eea-115">PARAMETERS</span></span>

### <span data-ttu-id="a1eea-116">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a1eea-116">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="a1eea-117">Az elsődleges védelmi tárolót adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1eea-117">Specifies a primary protection container.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1eea-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="a1eea-118">-Profile</span></span>
<span data-ttu-id="a1eea-119">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="a1eea-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a1eea-120">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="a1eea-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a1eea-121">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="a1eea-121">-ProtectionProfile</span></span>
<span data-ttu-id="a1eea-122">Itt adhatja meg a védelemi profil beállításait a védett tárolókkal való társításhoz.</span><span class="sxs-lookup"><span data-stu-id="a1eea-122">Specifies the protection profile settings to disassociate from the protection containers.</span></span>
<span data-ttu-id="a1eea-123">Itt adhatja meg a védett tárolók védelmi profiljának beállításait.</span><span class="sxs-lookup"><span data-stu-id="a1eea-123">Specifies the protection profile settings to apply to the protection containers.</span></span>
<span data-ttu-id="a1eea-124">**ASRProtectionProfile** objektum beolvasásához használja az New-AzureSiteRecoveryProtectionProfileObject parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a1eea-124">To obtain an **ASRProtectionProfile** object, use the New-AzureSiteRecoveryProtectionProfileObject cmdlet.</span></span>

```yaml
Type: ASRProtectionProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1eea-125">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a1eea-125">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="a1eea-126">A helyreállítási védelmi tárolót adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1eea-126">Specifies a recovery protection container.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1eea-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1eea-127">CommonParameters</span></span>
<span data-ttu-id="a1eea-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a1eea-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1eea-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1eea-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1eea-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1eea-130">INPUTS</span></span>

## <span data-ttu-id="a1eea-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1eea-131">OUTPUTS</span></span>

## <span data-ttu-id="a1eea-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a1eea-132">NOTES</span></span>

## <span data-ttu-id="a1eea-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1eea-133">RELATED LINKS</span></span>

[<span data-ttu-id="a1eea-134">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a1eea-134">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="a1eea-135">Új – AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="a1eea-135">New-AzureSiteRecoveryProtectionProfileObject</span></span>](./New-AzureSiteRecoveryProtectionProfileObject.md)

[<span data-ttu-id="a1eea-136">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span><span class="sxs-lookup"><span data-stu-id="a1eea-136">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span></span>](./Start-AzureSiteRecoveryProtectionProfileAssociationJob.md)


