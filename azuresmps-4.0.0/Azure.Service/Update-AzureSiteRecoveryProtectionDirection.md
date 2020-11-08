---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 870EE77E-57D9-4B52-9F80-CB24D642E6E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4f94d95b40fb89f0c1df89ad0c8a9b78eb283184
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016400"
---
# <span data-ttu-id="ae3fc-101">Update-AzureSiteRecoveryProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="ae3fc-101">Update-AzureSiteRecoveryProtectionDirection</span></span>

## <span data-ttu-id="ae3fc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ae3fc-102">SYNOPSIS</span></span>
<span data-ttu-id="ae3fc-103">A forrás-és a célkiszolgáló frissítése egy webhely-helyreállítási objektum védelmére.</span><span class="sxs-lookup"><span data-stu-id="ae3fc-103">Updates the source and target server for the protection of a Site Recovery object.</span></span>

## <span data-ttu-id="ae3fc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ae3fc-104">SYNTAX</span></span>

### <span data-ttu-id="ae3fc-105">ByRPObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ae3fc-105">ByRPObject (Default)</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ae3fc-106">ByRPId</span><span class="sxs-lookup"><span data-stu-id="ae3fc-106">ByRPId</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -RPId <String> -Direction <String> [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ae3fc-107">ByPEId</span><span class="sxs-lookup"><span data-stu-id="ae3fc-107">ByPEId</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ae3fc-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="ae3fc-108">ByPEObject</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ae3fc-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="ae3fc-109">DESCRIPTION</span></span>
<span data-ttu-id="ae3fc-110">Az **Update-AzureSiteRecoveryProtectionDirection** parancsmag frissíti a forrás-és célkiszolgáló tartalmát az Azure-webhely helyreállítási objektumának védelmére a véglegesítést követő feladatátvételi művelet befejezése után.</span><span class="sxs-lookup"><span data-stu-id="ae3fc-110">The **Update-AzureSiteRecoveryProtectionDirection** cmdlet updates the source and target server for the protection of an Azure Site Recovery object after a commit failover operation finishes.</span></span>

## <span data-ttu-id="ae3fc-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ae3fc-111">EXAMPLES</span></span>

### <span data-ttu-id="ae3fc-112">Példa 1: a védett objektum irányának módosítása egy tárolóban</span><span class="sxs-lookup"><span data-stu-id="ae3fc-112">Example 1: Modify the direction for a protected object in a container</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container  
PS C:\> Update-AzureSiteRecoveryProtectionDirection -Direction RecoveryToPrimary -ProtectionEntity $Protected 
ID               : c38eecdc-731c-405b-a61c-08db99aae2fe
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : {}
Name             : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="ae3fc-113">Az első parancs a **Get-AzureSiteRecoveryProtectionContainer** parancsmag használatával kapja meg a védett tárolókat az aktuális Azure-webhely helyreállítási pincéjében, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ae3fc-113">The first command gets the protected containers in the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="ae3fc-114">A második parancs a **Get-AzureSiteRecoveryProtectionEntity** parancsmaggal a $Containerban tárolt tárolóhoz tartozó virtuális gépeket kapja.</span><span class="sxs-lookup"><span data-stu-id="ae3fc-114">The second command gets the virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="ae3fc-115">A parancs az eredményt a $Protected változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ae3fc-115">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="ae3fc-116">A végleges parancs a $Protected-ban tárolt objektumok irányát RecoverToPrimary állítja be.</span><span class="sxs-lookup"><span data-stu-id="ae3fc-116">The final command sets the direction to RecoverToPrimary for the objects stored in $Protected.</span></span>

## <span data-ttu-id="ae3fc-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ae3fc-117">PARAMETERS</span></span>

### <span data-ttu-id="ae3fc-118">-Irány</span><span class="sxs-lookup"><span data-stu-id="ae3fc-118">-Direction</span></span>
<span data-ttu-id="ae3fc-119">A véglegesítés irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae3fc-119">Specifies the direction of the commit.</span></span>
<span data-ttu-id="ae3fc-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ae3fc-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae3fc-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="ae3fc-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="ae3fc-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="ae3fc-122">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae3fc-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="ae3fc-123">-Profile</span></span>
<span data-ttu-id="ae3fc-124">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="ae3fc-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ae3fc-125">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="ae3fc-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ae3fc-126">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="ae3fc-126">-ProtectionContainerId</span></span>
<span data-ttu-id="ae3fc-127">Egy védett tároló AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae3fc-127">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="ae3fc-128">Ez a parancsmag módosítja egy védett virtuális gép irányát, amely a paraméter által megadott tárolóhoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="ae3fc-128">This cmdlet modifies the direction for a protected virtual machine that belongs to the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae3fc-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="ae3fc-129">-ProtectionEntity</span></span>
<span data-ttu-id="ae3fc-130">A védelmi entitás objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae3fc-130">Specifies the protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae3fc-131">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="ae3fc-131">-ProtectionEntityId</span></span>
<span data-ttu-id="ae3fc-132">Egy védett virtuális gép AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae3fc-132">Specifies the ID of a protected virtual machine.</span></span>
<span data-ttu-id="ae3fc-133">Ez a parancsmag módosítja a védett virtuális gép irányát, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae3fc-133">This cmdlet modifies the direction for the protected virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae3fc-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ae3fc-134">-RecoveryPlan</span></span>
<span data-ttu-id="ae3fc-135">A helyreállítási terv objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae3fc-135">Specifies a recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae3fc-136">-RPId</span><span class="sxs-lookup"><span data-stu-id="ae3fc-136">-RPId</span></span>
<span data-ttu-id="ae3fc-137">A helyreállítási terv AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae3fc-137">Specifies the ID of a recovery plan.</span></span>
<span data-ttu-id="ae3fc-138">Ez a parancsmag módosítja a paraméter által megadott helyreállítási terv irányát.</span><span class="sxs-lookup"><span data-stu-id="ae3fc-138">This cmdlet modifies the direction for the recovery plan that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae3fc-139">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="ae3fc-139">-WaitForCompletion</span></span>
<span data-ttu-id="ae3fc-140">Azt jelzi, hogy a parancsmag a művelet befejezéséhez vár, mielőtt a vezérlőt visszaadja a Windows PowerShell konzolnak.</span><span class="sxs-lookup"><span data-stu-id="ae3fc-140">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae3fc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae3fc-141">CommonParameters</span></span>
<span data-ttu-id="ae3fc-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ae3fc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae3fc-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae3fc-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae3fc-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae3fc-144">INPUTS</span></span>

## <span data-ttu-id="ae3fc-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae3fc-145">OUTPUTS</span></span>

## <span data-ttu-id="ae3fc-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ae3fc-146">NOTES</span></span>

## <span data-ttu-id="ae3fc-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae3fc-147">RELATED LINKS</span></span>

[<span data-ttu-id="ae3fc-148">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ae3fc-148">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="ae3fc-149">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="ae3fc-149">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


