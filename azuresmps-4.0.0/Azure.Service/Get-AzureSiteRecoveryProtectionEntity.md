---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CB1A36E9-75BE-43CF-9092-9713DFEB96F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5329d50f87b92254136c222f406bb49586d6d7a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015588"
---
# <span data-ttu-id="d01ad-101">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="d01ad-101">Get-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="d01ad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d01ad-102">SYNOPSIS</span></span>
<span data-ttu-id="d01ad-103">Védett vagy védett entitásokat kap a webhely-helyreállítási boltozatban.</span><span class="sxs-lookup"><span data-stu-id="d01ad-103">Gets protectable or protected entities in a Site Recovery vault.</span></span>

## <span data-ttu-id="d01ad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d01ad-104">SYNTAX</span></span>

### <span data-ttu-id="d01ad-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d01ad-105">ByObject (Default)</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="d01ad-106">ByObjectWithId</span><span class="sxs-lookup"><span data-stu-id="d01ad-106">ByObjectWithId</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d01ad-107">ByIDsWithId</span><span class="sxs-lookup"><span data-stu-id="d01ad-107">ByIDsWithId</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="d01ad-108">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="d01ad-108">ByObjectWithName</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d01ad-109">ByIDsWithName</span><span class="sxs-lookup"><span data-stu-id="d01ad-109">ByIDsWithName</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Name <String> -ProtectionContainerId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d01ad-110">ByIDs</span><span class="sxs-lookup"><span data-stu-id="d01ad-110">ByIDs</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d01ad-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="d01ad-111">DESCRIPTION</span></span>
<span data-ttu-id="d01ad-112">A **Get-AzureSiteRecoveryProtectionEntity** parancsmag a védett vagy a védett entitásokat, például a virtuális gépeket a jelenlegi Azure webhely-helyreállítási boltozatban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d01ad-112">The **Get-AzureSiteRecoveryProtectionEntity** cmdlet gets the protectable or protected entities, such as virtual machines, in the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="d01ad-113">Példák</span><span class="sxs-lookup"><span data-stu-id="d01ad-113">EXAMPLES</span></span>

### <span data-ttu-id="d01ad-114">Példa 1: védett virtuális gép megjelenítése tárolóban</span><span class="sxs-lookup"><span data-stu-id="d01ad-114">Example 1: Display a protected virtual machine in a container</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer
PS C:\> Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
ID                           : 43aaab46-1cb0-4c39-8077-9a091c3b05ce
ServerId                     : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c
ProtectionContainerId        : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c_1c513d45-645d-4ed0-b9ae-e7b869a1f7fc
Name                         : testvm
Type                         : VirtualMachine
FabricObjectId               : 506B3CAC-5758-49E2-98C4-E5B0512E4D8E
Protected                    : False
CanCommit                    : False
CanFailover                  : False
CanReverseReplicate          : False
ActiveLocation               : Primary
ProtectionStateDescription   : Enabling protection
ReplicationHealth            : 
TestFailoverStateDescription : Nonev
ReplicationProvider          : HyperVReplica
```

<span data-ttu-id="d01ad-115">Az első parancs a **Get-AzureSiteRecoveryProtectionContainer** parancsmag használatával kap védett tárolót, majd az objektumot a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d01ad-115">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that object in the $Container variable.</span></span>

<span data-ttu-id="d01ad-116">A második parancs a védett virtuális gépet kapja, amely az $Container tárolóhoz tartozik, majd megjeleníti.</span><span class="sxs-lookup"><span data-stu-id="d01ad-116">The second command gets the protected virtual machine that belongs to the container in $Container, and then displays it.</span></span>

## <span data-ttu-id="d01ad-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d01ad-117">PARAMETERS</span></span>

### <span data-ttu-id="d01ad-118">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="d01ad-118">-Id</span></span>
<span data-ttu-id="d01ad-119">A beolvasott védelmi entitás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d01ad-119">Specifies the ID of a protection entity to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithId, ByIDsWithId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01ad-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d01ad-120">-Name</span></span>
<span data-ttu-id="d01ad-121">A beolvasott védelmi entitás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d01ad-121">Specifies the name of a protection entity to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName, ByIDsWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01ad-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="d01ad-122">-Profile</span></span>
<span data-ttu-id="d01ad-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d01ad-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d01ad-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d01ad-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d01ad-125">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d01ad-125">-ProtectionContainer</span></span>
<span data-ttu-id="d01ad-126">Egy védelmi tárolót ad meg.</span><span class="sxs-lookup"><span data-stu-id="d01ad-126">Specifies a protection container.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObjectWithId, ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d01ad-127">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="d01ad-127">-ProtectionContainerId</span></span>
<span data-ttu-id="d01ad-128">Egy védett tároló AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d01ad-128">Specifies the ID of a protected container.</span></span>

```yaml
Type: String
Parameter Sets: ByIDsWithId, ByIDsWithName, ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01ad-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d01ad-129">CommonParameters</span></span>
<span data-ttu-id="d01ad-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d01ad-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d01ad-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d01ad-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d01ad-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d01ad-132">INPUTS</span></span>

## <span data-ttu-id="d01ad-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d01ad-133">OUTPUTS</span></span>

## <span data-ttu-id="d01ad-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d01ad-134">NOTES</span></span>

## <span data-ttu-id="d01ad-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d01ad-135">RELATED LINKS</span></span>

[<span data-ttu-id="d01ad-136">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d01ad-136">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="d01ad-137">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="d01ad-137">Set-AzureSiteRecoveryProtectionEntity</span></span>](./Set-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="d01ad-138">Update-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="d01ad-138">Update-AzureSiteRecoveryProtectionEntity</span></span>](./Update-AzureSiteRecoveryProtectionEntity.md)


