---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C263CCAD-E51F-420E-9AD4-4FAC09C99CB1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3c10a7694034fe4400ed415891e74f7089ce8558
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016112"
---
# <span data-ttu-id="0b909-101">Remove-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="0b909-101">Remove-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="0b909-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0b909-102">SYNOPSIS</span></span>
<span data-ttu-id="0b909-103">Eltávolítja a felhőalapú szolgáltatás távoli asztali bővítményét, amelyet az összes szerepkör vagy elnevezett szerepkör a megadott központi telepítő bővítőhelyen alkalmazott.</span><span class="sxs-lookup"><span data-stu-id="0b909-103">Removes the cloud service remote desktop extension applied on all roles or named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="0b909-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0b909-104">SYNTAX</span></span>

### <span data-ttu-id="0b909-105">RemoveByRoles (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0b909-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b909-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="0b909-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>]
 [-UninstallConfiguration] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0b909-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0b909-107">DESCRIPTION</span></span>
<span data-ttu-id="0b909-108">A **Remove-AzureServiceRemoteDesktopExtension** parancsmag eltávolítja a felhőalapú szolgáltatás távoli asztali bővítményét az összes szerepkörön vagy elnevezett szerepkörökön egy bizonyos központi telepítő bővítőhelyen.</span><span class="sxs-lookup"><span data-stu-id="0b909-108">The **Remove-AzureServiceRemoteDesktopExtension** cmdlet removes the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="0b909-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0b909-109">EXAMPLES</span></span>

### <span data-ttu-id="0b909-110">1. példa: a távoli asztali bővítmény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0b909-110">Example 1: Remove the remote desktop extension</span></span>
```
PS C:\> Remove-AzureServiceRemoteDesktopExtension -ServiceName $svc
```

<span data-ttu-id="0b909-111">Ez a parancs eltávolítja a távoli asztali bővítményt.</span><span class="sxs-lookup"><span data-stu-id="0b909-111">This command removes the remote desktop extension.</span></span>

### <span data-ttu-id="0b909-112">2. példa: a távoli asztali bővítmény eltávolítása meghatározott szerepkörről</span><span class="sxs-lookup"><span data-stu-id="0b909-112">Example 2: Remove the remote desktop extension from a specified role</span></span>
```
PS C:\> Remove-AzureServiceRemoteDesktopExtension -ServiceName $svc -Role "WebRole1"
```

<span data-ttu-id="0b909-113">Ez a parancs eltávolítja a távoli asztali bővítményt egy adott szerepkörből.</span><span class="sxs-lookup"><span data-stu-id="0b909-113">This command removes the remote desktop extension from a specified role.</span></span>

## <span data-ttu-id="0b909-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0b909-114">PARAMETERS</span></span>

### <span data-ttu-id="0b909-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0b909-115">-InformationAction</span></span>
<span data-ttu-id="0b909-116">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="0b909-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0b909-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0b909-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0b909-118">Folytassa</span><span class="sxs-lookup"><span data-stu-id="0b909-118">Continue</span></span>
- <span data-ttu-id="0b909-119">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="0b909-119">Ignore</span></span>
- <span data-ttu-id="0b909-120">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="0b909-120">Inquire</span></span>
- <span data-ttu-id="0b909-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0b909-121">SilentlyContinue</span></span>
- <span data-ttu-id="0b909-122">állj</span><span class="sxs-lookup"><span data-stu-id="0b909-122">Stop</span></span>
- <span data-ttu-id="0b909-123">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="0b909-123">Suspend</span></span>

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

### <span data-ttu-id="0b909-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0b909-124">-InformationVariable</span></span>
<span data-ttu-id="0b909-125">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="0b909-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0b909-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="0b909-126">-Profile</span></span>
<span data-ttu-id="0b909-127">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="0b909-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0b909-128">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="0b909-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0b909-129">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="0b909-129">-Role</span></span>
<span data-ttu-id="0b909-130">A szerepkörök választható tömbjét adja meg a távoli asztali konfiguráció megadásához.</span><span class="sxs-lookup"><span data-stu-id="0b909-130">Specifies an optional array of roles to specify the remote desktop configuration for.</span></span>
<span data-ttu-id="0b909-131">Ha nincs megadva, a program az összes szerepkör alapértelmezett konfigurációjának megfelelően alkalmazza a távoli asztali konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="0b909-131">If not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: RemoveByRoles
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b909-132">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="0b909-132">-ServiceName</span></span>
<span data-ttu-id="0b909-133">A központi üzembe helyezés Azure-szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b909-133">Specifies the Azure service name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b909-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="0b909-134">-Slot</span></span>
<span data-ttu-id="0b909-135">A módosítani kívánt központi verzió környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b909-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="0b909-136">A támogatott értékek a "termelés" vagy a "megállóhely".</span><span class="sxs-lookup"><span data-stu-id="0b909-136">Supported values are "Production" or "Staging".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b909-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b909-137">-UninstallConfiguration</span></span>
<span data-ttu-id="0b909-138">Azt adja meg, hogy a parancsmag eltávolítja a felhőalapú szolgáltatásból az összes RDP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="0b909-138">Specifies that this cmdlet uninstalls all RDP configurations from the cloud service.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAllRoles
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b909-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b909-139">CommonParameters</span></span>
<span data-ttu-id="0b909-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0b909-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b909-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b909-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b909-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b909-142">INPUTS</span></span>

## <span data-ttu-id="0b909-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b909-143">OUTPUTS</span></span>

## <span data-ttu-id="0b909-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0b909-144">NOTES</span></span>

## <span data-ttu-id="0b909-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b909-145">RELATED LINKS</span></span>

[<span data-ttu-id="0b909-146">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="0b909-146">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


