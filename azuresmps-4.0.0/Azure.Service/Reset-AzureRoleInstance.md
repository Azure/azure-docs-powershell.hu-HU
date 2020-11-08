---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2AEA385F-E180-4564-A62A-9E913C665801
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fff3ea97c51ee5597e585f3275b25e513c22008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015480"
---
# <span data-ttu-id="41c78-101">Reset-AzureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="41c78-101">Reset-AzureRoleInstance</span></span>

## <span data-ttu-id="41c78-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41c78-102">SYNOPSIS</span></span>
<span data-ttu-id="41c78-103">Egyetlen szerepkör-példány vagy egy adott szerepkör minden szerepkör-példányának újraindítását vagy visszavonását kéri.</span><span class="sxs-lookup"><span data-stu-id="41c78-103">Requests a reboot or reimage of a single role instance or all role instances of a specific role.</span></span>

## <span data-ttu-id="41c78-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41c78-104">SYNTAX</span></span>

```
Reset-AzureRoleInstance [-ServiceName] <String> -Slot <String> -InstanceName <String> [-Reboot] [-Reimage]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="41c78-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="41c78-105">DESCRIPTION</span></span>
<span data-ttu-id="41c78-106">A **reset-AzureRoleInstance** parancsmag a bevezetésben futó szerepkör-példány újraindítását vagy átállítását kéri.</span><span class="sxs-lookup"><span data-stu-id="41c78-106">The **Reset-AzureRoleInstance** cmdlet requests a reboot or a reimage of a role instance that is running in a deployment.</span></span>
<span data-ttu-id="41c78-107">Ez a művelet szinkron módon fut.</span><span class="sxs-lookup"><span data-stu-id="41c78-107">This operation executes synchronously.</span></span>
<span data-ttu-id="41c78-108">Egy szerepkör-példány újraindításakor az Azure a példány offline állapotba kerül, újraindul a példány mögöttes operációs rendszer, és a példány visszakerül az internethez.</span><span class="sxs-lookup"><span data-stu-id="41c78-108">When you reboot a role instance, Azure takes the instance offline, restarts the underlying operating system for that instance, and brings the instance back online.</span></span>
<span data-ttu-id="41c78-109">Minden olyan adatot, amely a helyi lemezre íródott, továbbra is elérhető lesz az újraindítások között.</span><span class="sxs-lookup"><span data-stu-id="41c78-109">Any data that is written to the local disk persists across reboots.</span></span>
<span data-ttu-id="41c78-110">A memóriában lévő összes adatot elvész.</span><span class="sxs-lookup"><span data-stu-id="41c78-110">Any data that is in-memory is lost.</span></span>

<span data-ttu-id="41c78-111">A szerepkör-példányok újraképkezelése eltérő viselkedést eredményez a szerepkör típusától függően.</span><span class="sxs-lookup"><span data-stu-id="41c78-111">Reimaging a role instance results in different behavior depending on the type of role.</span></span>
<span data-ttu-id="41c78-112">Ha a szerepkört áthelyezi a webhelyre vagy a munkatársi szerepkörre, az Azure a szerepkört offline állapotba helyezi, és az Azure Guest operációs rendszer új példányát írja a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="41c78-112">For a web or worker role, when the role is reimaged, Azure takes the role offline and writes a fresh installation of the Azure guest operating system to the virtual machine.</span></span>
<span data-ttu-id="41c78-113">A szerepkör ezután ismét online állapotba kerül.</span><span class="sxs-lookup"><span data-stu-id="41c78-113">The role is then brought back online.</span></span>
<span data-ttu-id="41c78-114">VM-szerep esetén az Azure a szerepkör kapcsolat nélküli állapotba helyezése után újra alkalmazza a szerepkört az Ön által megadott egyéni képfájlra, és ismét online állapotba hozza a szerepkört.</span><span class="sxs-lookup"><span data-stu-id="41c78-114">For a VM role, when the role is reimaged, Azure takes the role offline, reapplies the custom image that you provided for it, and brings the role back online.</span></span>

<span data-ttu-id="41c78-115">Az Azure megkísérli a szerepkör átadásakor a helyi tárterület-erőforrásokban tárolt adatok megőrzését; átmeneti hardverhiba esetén azonban előfordulhat, hogy a helyi tárterület-erőforrás elveszhet.</span><span class="sxs-lookup"><span data-stu-id="41c78-115">Azure attempts to maintain data in any local storage resources when the role is reimaged; however, in case of a transient hardware failure, the local storage resource may be lost.</span></span>
<span data-ttu-id="41c78-116">Ha az alkalmazás az adatmegőrzést igényli, a tartós adatforrásba (például Azure-meghajtóra) való írás ajánlott.</span><span class="sxs-lookup"><span data-stu-id="41c78-116">If your application requires that data persist, writing to a durable data source, such as an Azure drive, is recommended.</span></span>
<span data-ttu-id="41c78-117">Bármely olyan adat, amely a helyi tárterület-erőforrás által definiált eltérő helyi címtárba íródott, elvész, amikor a szerepkört átadta.</span><span class="sxs-lookup"><span data-stu-id="41c78-117">Any data that is written to a local directory other than that defined by the local storage resource will be lost when the role is reimaged.</span></span>

## <span data-ttu-id="41c78-118">Példák</span><span class="sxs-lookup"><span data-stu-id="41c78-118">EXAMPLES</span></span>

### <span data-ttu-id="41c78-119">1. példa: egy szerepkör-példány újraindítása</span><span class="sxs-lookup"><span data-stu-id="41c78-119">Example 1: Reboot a role instance</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -InstanceName "MyWebRole_IN_0" -Reboot
```

<span data-ttu-id="41c78-120">Ez a parancs újraindítja a MyWebRole_IN_0 nevű szerepkör-példányt a MySvc01 szolgáltatás bevezetési példányában.</span><span class="sxs-lookup"><span data-stu-id="41c78-120">This command reboots the role instance named MyWebRole_IN_0 in the staging deployment of the MySvc01 service.</span></span>

### <span data-ttu-id="41c78-121">2. példa: egy szerepkör-példány visszakeresése</span><span class="sxs-lookup"><span data-stu-id="41c78-121">Example 2: Reimage a role instance</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -Reimage
```

<span data-ttu-id="41c78-122">Ez a parancs a MySvc01-Felhőbeli szolgáltatás bevezetési példányának szerepkör-példányait.</span><span class="sxs-lookup"><span data-stu-id="41c78-122">This command reimages the role instances in the staging deployment of the MySvc01 cloud service.</span></span>

### <span data-ttu-id="41c78-123">3. példa: a minden szerepkör-példány visszakeresése</span><span class="sxs-lookup"><span data-stu-id="41c78-123">Example 3: Reimage all role instances</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc1" -Slot "Production" -Reimage
```

<span data-ttu-id="41c78-124">Ez a parancs minden szerepkör-példányt átvesz a MySvc01 szolgáltatás üzembe helyezésére.</span><span class="sxs-lookup"><span data-stu-id="41c78-124">This command reimages all role instances in the production deployment of the MySvc01 service.</span></span>

## <span data-ttu-id="41c78-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41c78-125">PARAMETERS</span></span>

### <span data-ttu-id="41c78-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="41c78-126">-InformationAction</span></span>
<span data-ttu-id="41c78-127">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="41c78-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="41c78-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="41c78-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="41c78-129">Folytassa</span><span class="sxs-lookup"><span data-stu-id="41c78-129">Continue</span></span>
- <span data-ttu-id="41c78-130">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="41c78-130">Ignore</span></span>
- <span data-ttu-id="41c78-131">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="41c78-131">Inquire</span></span>
- <span data-ttu-id="41c78-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="41c78-132">SilentlyContinue</span></span>
- <span data-ttu-id="41c78-133">állj</span><span class="sxs-lookup"><span data-stu-id="41c78-133">Stop</span></span>
- <span data-ttu-id="41c78-134">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="41c78-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41c78-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="41c78-135">-InformationVariable</span></span>
<span data-ttu-id="41c78-136">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="41c78-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41c78-137">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="41c78-137">-InstanceName</span></span>
<span data-ttu-id="41c78-138">Annak a szerepkör-példánynak a nevét adja meg, amelybe át szeretné majd indítani a feladatot.</span><span class="sxs-lookup"><span data-stu-id="41c78-138">Specifies the name of the role instance to reimage or reboot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41c78-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="41c78-139">-Profile</span></span>
<span data-ttu-id="41c78-140">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="41c78-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="41c78-141">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="41c78-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="41c78-142">-Reboot</span><span class="sxs-lookup"><span data-stu-id="41c78-142">-Reboot</span></span>
<span data-ttu-id="41c78-143">Azt adja meg, hogy a parancsmag újraindítja a megadott szerepkör-példányt, vagy ha nincs megadva, az összes szerepkör-példány.</span><span class="sxs-lookup"><span data-stu-id="41c78-143">Specifies that this cmdlet reboots the specified role instance or, if none is specified, all role instances.</span></span>
<span data-ttu-id="41c78-144">Az *újraindítást* vagy a *Reimage* paramétert is tartalmaznia kell, de mindkettőt nem.</span><span class="sxs-lookup"><span data-stu-id="41c78-144">You must include either a *Reboot* or *Reimage* parameter, but not both.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41c78-145">-Reimage</span><span class="sxs-lookup"><span data-stu-id="41c78-145">-Reimage</span></span>
<span data-ttu-id="41c78-146">Itt adhatja meg, hogy a parancsmag a megadott szerepkör-példányt, vagy ha nincs megadva, az összes szerepkör-példányt átadja-e.</span><span class="sxs-lookup"><span data-stu-id="41c78-146">Specifies that this cmdlet reimages the specified role instance or, if none is specified, all role instances.</span></span>
<span data-ttu-id="41c78-147">Az *újraindítást* vagy a *Reimage* paramétert is tartalmaznia kell, de mindkettőt nem.</span><span class="sxs-lookup"><span data-stu-id="41c78-147">You must include either a *Reboot* or *Reimage* parameter, but not both.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41c78-148">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="41c78-148">-ServiceName</span></span>
<span data-ttu-id="41c78-149">A szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="41c78-149">Specifies the name of the service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41c78-150">-Slot</span><span class="sxs-lookup"><span data-stu-id="41c78-150">-Slot</span></span>
<span data-ttu-id="41c78-151">A szerepkör példányait futtató központi telepítő környezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="41c78-151">Specifies the deployment environment where the role instances run.</span></span>
<span data-ttu-id="41c78-152">Érvényes értékek: a termelés és a megállóhelyek.</span><span class="sxs-lookup"><span data-stu-id="41c78-152">Valid values are: Production and Staging.</span></span>
<span data-ttu-id="41c78-153">A *DeploymentName* vagy a *slot* paramétert is használhatja, de mindkettőt nem.</span><span class="sxs-lookup"><span data-stu-id="41c78-153">You can include either the *DeploymentName* or *Slot* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41c78-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41c78-154">CommonParameters</span></span>
<span data-ttu-id="41c78-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41c78-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41c78-156">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41c78-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41c78-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41c78-157">INPUTS</span></span>

## <span data-ttu-id="41c78-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41c78-158">OUTPUTS</span></span>

## <span data-ttu-id="41c78-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41c78-159">NOTES</span></span>

## <span data-ttu-id="41c78-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41c78-160">RELATED LINKS</span></span>

[<span data-ttu-id="41c78-161">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="41c78-161">Set-AzureRole</span></span>](./Set-AzureRole.md)


