---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 1415BBA3-3F55-46A9-B20B-DFA72342BDF4
online version: ''
schema: 2.0.0
ms.openlocfilehash: ec7883b996e5da367884fd7d051a5299c6d62a9e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016423"
---
# <span data-ttu-id="eceaf-101">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="eceaf-101">Set-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="eceaf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eceaf-102">SYNOPSIS</span></span>
<span data-ttu-id="eceaf-103">Beállítja a webhely-helyreállítási védelem entitás állapotát.</span><span class="sxs-lookup"><span data-stu-id="eceaf-103">Sets the state for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="eceaf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eceaf-104">SYNTAX</span></span>

### <span data-ttu-id="eceaf-105">ByPEObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eceaf-105">ByPEObject (Default)</span></span>
```
Set-AzureSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity>
 [-ProtectionProfile <ASRProtectionProfile>] -Protection <String> [-OSDiskName <String>] [-OS <String>]
 [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eceaf-106">ByIDs</span><span class="sxs-lookup"><span data-stu-id="eceaf-106">ByIDs</span></span>
```
Set-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainerId <String>
 [-ProtectionProfile <ASRProtectionProfile>] -Protection <String> [-OSDiskName <String>] [-OS <String>]
 [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eceaf-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="eceaf-107">DESCRIPTION</span></span>
<span data-ttu-id="eceaf-108">A **set-AzureSiteRecoveryProtectionEntity** parancsmag engedélyezi vagy letiltja a védelmet az Azure webhely-helyreállítási védelmi entitások számára.</span><span class="sxs-lookup"><span data-stu-id="eceaf-108">The **Set-AzureSiteRecoveryProtectionEntity** cmdlet enables or disables protection on an Azure Site Recovery protection entity.</span></span>

## <span data-ttu-id="eceaf-109">Példák</span><span class="sxs-lookup"><span data-stu-id="eceaf-109">EXAMPLES</span></span>

### <span data-ttu-id="eceaf-110">1. példa: védelem engedélyezése a tárolóban lévő objektumokhoz</span><span class="sxs-lookup"><span data-stu-id="eceaf-110">Example 1: Enable protection for objects in a container</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer -Name "Cloud17"
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer -Name "VM01"
PS C:\> Set-AzureSiteRecoveryProtectionEntity -ProtectionEntity $ ProtectionEntity -Protection Enable -ProtectionProfile $ProtectionContainer.AvailableProtectionProfiles[0] -OS Windows
```

<span data-ttu-id="eceaf-111">Az első parancs a **Get-AzureSiteRecoveryProtectionContainer** parancsmag segítségével az aktuális Azure-webhely tárolóit kapja, majd a $ProtectionContainer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="eceaf-111">The first command gets containers for the current Azure Site vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="eceaf-112">A második parancs a **Get-AzureSiteRecoveryProtectionEntity** parancsmaggal a $ProtectionContainer tárolt tárolóhoz tartozó védett virtuális gépeket kapja.</span><span class="sxs-lookup"><span data-stu-id="eceaf-112">The second command gets the protected virtual machines that belong to the container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="eceaf-113">A parancs az eredményt a $ProtectionEntity változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="eceaf-113">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="eceaf-114">A végleges parancs engedélyezi a $ProtectionEntityban tárolt entitások védelmét.</span><span class="sxs-lookup"><span data-stu-id="eceaf-114">The final command enables protection for the entities stored in $ProtectionEntity.</span></span>

## <span data-ttu-id="eceaf-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eceaf-115">PARAMETERS</span></span>

### <span data-ttu-id="eceaf-116">-Force</span><span class="sxs-lookup"><span data-stu-id="eceaf-116">-Force</span></span>
<span data-ttu-id="eceaf-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="eceaf-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eceaf-118">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="eceaf-118">-Id</span></span>
<span data-ttu-id="eceaf-119">Annak a védett virtuális gépnek az AZONOSÍTÓját adja meg, amely számára engedélyezni vagy letiltani szeretné a védelmet.</span><span class="sxs-lookup"><span data-stu-id="eceaf-119">Specifies the ID of a protected virtual machine for which to enable or disable protection.</span></span>

```yaml
Type: String
Parameter Sets: ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eceaf-120">-OS</span><span class="sxs-lookup"><span data-stu-id="eceaf-120">-OS</span></span>
<span data-ttu-id="eceaf-121">Az operációs rendszer típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="eceaf-121">Specifies the operating system type.</span></span>
<span data-ttu-id="eceaf-122">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="eceaf-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eceaf-123">Windows</span><span class="sxs-lookup"><span data-stu-id="eceaf-123">Windows</span></span>
- <span data-ttu-id="eceaf-124">Linux</span><span class="sxs-lookup"><span data-stu-id="eceaf-124">Linux</span></span>

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

### <span data-ttu-id="eceaf-125">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="eceaf-125">-OSDiskName</span></span>
<span data-ttu-id="eceaf-126">Az operációs rendszert tartalmazó lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eceaf-126">Specifies the name of the disk that contains the operating system.</span></span>

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

### <span data-ttu-id="eceaf-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="eceaf-127">-Profile</span></span>
<span data-ttu-id="eceaf-128">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="eceaf-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="eceaf-129">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="eceaf-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="eceaf-130">-Védelem</span><span class="sxs-lookup"><span data-stu-id="eceaf-130">-Protection</span></span>
<span data-ttu-id="eceaf-131">Megadja, hogy engedélyezve vagy le kell-e tiltani a védelmet.</span><span class="sxs-lookup"><span data-stu-id="eceaf-131">Specifies whether protection should be enabled or disabled.</span></span>
<span data-ttu-id="eceaf-132">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="eceaf-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eceaf-133">Engedélyezése</span><span class="sxs-lookup"><span data-stu-id="eceaf-133">Enable</span></span>
- <span data-ttu-id="eceaf-134">Megbénít</span><span class="sxs-lookup"><span data-stu-id="eceaf-134">Disable</span></span>

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

### <span data-ttu-id="eceaf-135">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="eceaf-135">-ProtectionContainerId</span></span>
<span data-ttu-id="eceaf-136">Egy védett tároló AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="eceaf-136">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="eceaf-137">Ez a parancsmag engedélyezi vagy tiltja a virtuális gép védelmét, amely a paraméter által megadott tárolóhoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="eceaf-137">This cmdlet enables or disables protection for a virtual machine that belongs to the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eceaf-138">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="eceaf-138">-ProtectionEntity</span></span>
<span data-ttu-id="eceaf-139">A védelmi entitás objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="eceaf-139">Specifies the protection entity object.</span></span>

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

### <span data-ttu-id="eceaf-140">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="eceaf-140">-ProtectionProfile</span></span>
<span data-ttu-id="eceaf-141">A védelem engedélyezésére szolgáló védelmi profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="eceaf-141">Specifies a protection profile to enable protection.</span></span>
<span data-ttu-id="eceaf-142">Adjon meg egy **ASRProtectionProfile** -objektumot, amely a társított védelmi tárolóban elérhető védelmi profilok egyike.</span><span class="sxs-lookup"><span data-stu-id="eceaf-142">Specify an **ASRProtectionProfile** object that is one of the available protection profiles in the associated protection container.</span></span>

```yaml
Type: ASRProtectionProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eceaf-143">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="eceaf-143">-WaitForCompletion</span></span>
<span data-ttu-id="eceaf-144">Azt jelzi, hogy a parancsmag a művelet befejezéséhez vár, mielőtt a vezérlőt visszaadja a Windows PowerShell konzolnak.</span><span class="sxs-lookup"><span data-stu-id="eceaf-144">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="eceaf-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eceaf-145">-Confirm</span></span>
<span data-ttu-id="eceaf-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eceaf-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eceaf-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eceaf-147">-WhatIf</span></span>
<span data-ttu-id="eceaf-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eceaf-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eceaf-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eceaf-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eceaf-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eceaf-150">CommonParameters</span></span>
<span data-ttu-id="eceaf-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eceaf-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eceaf-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eceaf-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eceaf-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eceaf-153">INPUTS</span></span>

## <span data-ttu-id="eceaf-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eceaf-154">OUTPUTS</span></span>

## <span data-ttu-id="eceaf-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eceaf-155">NOTES</span></span>

## <span data-ttu-id="eceaf-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eceaf-156">RELATED LINKS</span></span>

[<span data-ttu-id="eceaf-157">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="eceaf-157">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="eceaf-158">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="eceaf-158">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="eceaf-159">Update-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="eceaf-159">Update-AzureSiteRecoveryProtectionEntity</span></span>](./Update-AzureSiteRecoveryProtectionEntity.md)


