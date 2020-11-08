---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CE15E01D-5D86-4960-8E37-7757B35F4464
online version: ''
schema: 2.0.0
ms.openlocfilehash: a87a825249d7d7cda3fc2dc43a93869f8d869705
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016569"
---
# <span data-ttu-id="99b8c-101">Get-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="99b8c-101">Get-AzureSiteRecoveryVM</span></span>

## <span data-ttu-id="99b8c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99b8c-102">SYNOPSIS</span></span>
<span data-ttu-id="99b8c-103">Információt kap a webhely-helyreállítási felügyelt virtuális gépekről.</span><span class="sxs-lookup"><span data-stu-id="99b8c-103">Gets information about Site Recovery-managed virtual machines.</span></span>

## <span data-ttu-id="99b8c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99b8c-104">SYNTAX</span></span>

### <span data-ttu-id="99b8c-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="99b8c-105">ByObject (Default)</span></span>
```
Get-AzureSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="99b8c-106">ByObjectWithId</span><span class="sxs-lookup"><span data-stu-id="99b8c-106">ByObjectWithId</span></span>
```
Get-AzureSiteRecoveryVM -Id <String> -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="99b8c-107">ByIDsWithId</span><span class="sxs-lookup"><span data-stu-id="99b8c-107">ByIDsWithId</span></span>
```
Get-AzureSiteRecoveryVM -Id <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="99b8c-108">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="99b8c-108">ByObjectWithName</span></span>
```
Get-AzureSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="99b8c-109">ByIDsWithName</span><span class="sxs-lookup"><span data-stu-id="99b8c-109">ByIDsWithName</span></span>
```
Get-AzureSiteRecoveryVM -Name <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="99b8c-110">ByIDs</span><span class="sxs-lookup"><span data-stu-id="99b8c-110">ByIDs</span></span>
```
Get-AzureSiteRecoveryVM -ProtectionContainerId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="99b8c-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="99b8c-111">DESCRIPTION</span></span>
<span data-ttu-id="99b8c-112">A **Get-AzureSiteRecoveryVM** parancsmag információt kap az Azure webhely-helyreállítással kezelt virtuális gépekről.</span><span class="sxs-lookup"><span data-stu-id="99b8c-112">The **Get-AzureSiteRecoveryVM** cmdlet gets information about virtual machines managed in Azure Site Recovery.</span></span>

## <span data-ttu-id="99b8c-113">Példák</span><span class="sxs-lookup"><span data-stu-id="99b8c-113">EXAMPLES</span></span>

### <span data-ttu-id="99b8c-114">Példa 1: információ kérése egy virtuális gépre</span><span class="sxs-lookup"><span data-stu-id="99b8c-114">Example 1: Get information about a virtual machine</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> Get-AzureSiteRecoveryVM -ProtectionContainer $ProtectionContainer
ID                          : a205fd17-3848-4896-bab6-9dbccc3cd8ed
ServerId                    : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c
ProtectionContainerId       : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c_1c513d45-645d-4ed0-b9ae-e7b869a1f7fc
Name                        : vm1
Type                        : VirtualMachine
FabricObjectId              : 86447b9e-d877-4e9a-8302-adcd6bbf18c0
Protected                   : False
CanCommit                   : False
CanFailover                 : True
CanReverseReplicate         : False
ActiveLocation              : Primary
ProtectionState             : Enabled
ReplicationHealth           : Healthy
TestFailoverState           : None
ReplicationProvider         : HyperVReplica
```

<span data-ttu-id="99b8c-115">Az első parancs a **Get-AzureSiteRecoveryProtectionContainer** parancsmagot használja a védett tároló beszerzéséhez, majd a $ProtectionContainer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="99b8c-115">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="99b8c-116">A második parancs információkat kap az $ProtectionContainer virtuális gépeiról.</span><span class="sxs-lookup"><span data-stu-id="99b8c-116">The second command gets information about the virtual machines in $ProtectionContainer.</span></span>

## <span data-ttu-id="99b8c-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99b8c-117">PARAMETERS</span></span>

### <span data-ttu-id="99b8c-118">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="99b8c-118">-Id</span></span>
<span data-ttu-id="99b8c-119">Annak a virtuális gépnek az AZONOSÍTÓját adja meg, amelyről információt szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="99b8c-119">Specifies the ID of the virtual machine about which to get information.</span></span>

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

### <span data-ttu-id="99b8c-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="99b8c-120">-Name</span></span>
<span data-ttu-id="99b8c-121">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="99b8c-121">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="99b8c-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="99b8c-122">-Profile</span></span>
<span data-ttu-id="99b8c-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="99b8c-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="99b8c-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="99b8c-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="99b8c-125">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="99b8c-125">-ProtectionContainer</span></span>
<span data-ttu-id="99b8c-126">A webhely-helyreállítási védelem tárolójának objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="99b8c-126">Specifies the Site Recovery protection container object.</span></span>

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

### <span data-ttu-id="99b8c-127">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="99b8c-127">-ProtectionContainerId</span></span>
<span data-ttu-id="99b8c-128">Annak a védett tárolónak az AZONOSÍTÓját adja meg, amelyről információt szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="99b8c-128">Specifies the ID of a protected container about which to get information.</span></span>

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

### <span data-ttu-id="99b8c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99b8c-129">CommonParameters</span></span>
<span data-ttu-id="99b8c-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99b8c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99b8c-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99b8c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99b8c-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99b8c-132">INPUTS</span></span>

## <span data-ttu-id="99b8c-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99b8c-133">OUTPUTS</span></span>

## <span data-ttu-id="99b8c-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99b8c-134">NOTES</span></span>

## <span data-ttu-id="99b8c-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99b8c-135">RELATED LINKS</span></span>

[<span data-ttu-id="99b8c-136">Set-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="99b8c-136">Set-AzureSiteRecoveryVM</span></span>](./Set-AzureSiteRecoveryVM.md)


