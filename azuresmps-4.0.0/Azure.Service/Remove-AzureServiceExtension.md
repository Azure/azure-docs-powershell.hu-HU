---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6B5E4968-5DF5-4956-A070-9F54A79D960B
online version: ''
schema: 2.0.0
ms.openlocfilehash: f45e0a93b2f6261ca6031aa721bda3a72f4443dd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016113"
---
# <span data-ttu-id="19c1a-101">Remove-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="19c1a-101">Remove-AzureServiceExtension</span></span>

## <span data-ttu-id="19c1a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19c1a-102">SYNOPSIS</span></span>
<span data-ttu-id="19c1a-103">Eltávolítja a központi üzembe helyezés során alkalmazott felhőalapú szolgáltatási bővítményeket.</span><span class="sxs-lookup"><span data-stu-id="19c1a-103">Removes cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="19c1a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19c1a-104">SYNTAX</span></span>

### <span data-ttu-id="19c1a-105">RemoveByRoles (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="19c1a-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-ExtensionName] <String> [-ProviderNamespace] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="19c1a-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="19c1a-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-UninstallConfiguration] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="19c1a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="19c1a-107">DESCRIPTION</span></span>
<span data-ttu-id="19c1a-108">A **Remove-AzureServiceExtension** parancsmag eltávolítja a központi telepítésen alkalmazott felhőalapú szolgáltatási bővítményeket.</span><span class="sxs-lookup"><span data-stu-id="19c1a-108">The **Remove-AzureServiceExtension** cmdlet removes cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="19c1a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="19c1a-109">EXAMPLES</span></span>

### <span data-ttu-id="19c1a-110">1. példa: a szolgáltatás bővítményének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="19c1a-110">Example 1: Remove a service extension</span></span>
```
PS C:\> Remove-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions"
```

<span data-ttu-id="19c1a-111">Ez a parancs eltávolítja a szolgáltatás-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="19c1a-111">This command removes a service extension.</span></span>

### <span data-ttu-id="19c1a-112">2. példa: a szolgáltatás-kiterjesztés eltávolítása és az összes konfiguráció eltávolítása</span><span class="sxs-lookup"><span data-stu-id="19c1a-112">Example 2: Remove a service extension and uninstall all configurations</span></span>
```
PS C:\> Remove-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -UninstallConfiguration
```

<span data-ttu-id="19c1a-113">Ez a parancs eltávolítja a szolgáltatás-kiterjesztést, és eltávolítja az összes konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="19c1a-113">This command removes a service extension and uninstalls all configurations.</span></span>

## <span data-ttu-id="19c1a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19c1a-114">PARAMETERS</span></span>

### <span data-ttu-id="19c1a-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="19c1a-115">-ExtensionName</span></span>
<span data-ttu-id="19c1a-116">A kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="19c1a-116">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19c1a-117">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="19c1a-117">-InformationAction</span></span>
<span data-ttu-id="19c1a-118">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="19c1a-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="19c1a-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="19c1a-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="19c1a-120">Folytassa</span><span class="sxs-lookup"><span data-stu-id="19c1a-120">Continue</span></span>
- <span data-ttu-id="19c1a-121">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="19c1a-121">Ignore</span></span>
- <span data-ttu-id="19c1a-122">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="19c1a-122">Inquire</span></span>
- <span data-ttu-id="19c1a-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="19c1a-123">SilentlyContinue</span></span>
- <span data-ttu-id="19c1a-124">állj</span><span class="sxs-lookup"><span data-stu-id="19c1a-124">Stop</span></span>
- <span data-ttu-id="19c1a-125">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="19c1a-125">Suspend</span></span>

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

### <span data-ttu-id="19c1a-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="19c1a-126">-InformationVariable</span></span>
<span data-ttu-id="19c1a-127">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="19c1a-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="19c1a-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="19c1a-128">-Profile</span></span>
<span data-ttu-id="19c1a-129">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="19c1a-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="19c1a-130">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="19c1a-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="19c1a-131">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="19c1a-131">-ProviderNamespace</span></span>
<span data-ttu-id="19c1a-132">A bővítmény-szolgáltató névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="19c1a-132">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19c1a-133">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="19c1a-133">-Role</span></span>
<span data-ttu-id="19c1a-134">A szerepkörök választható tömböket adja meg a kiterjesztés megadásához.</span><span class="sxs-lookup"><span data-stu-id="19c1a-134">Specifies an optional array of roles to specify the extension for.</span></span>
<span data-ttu-id="19c1a-135">Ha nincs megadva, a program az összes szerepkör alapértelmezett konfigurációjának a bővítményt alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="19c1a-135">If not specified the extension is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="19c1a-136">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="19c1a-136">-ServiceName</span></span>
<span data-ttu-id="19c1a-137">A felhőalapú szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="19c1a-137">Specifies the cloud service name.</span></span>

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

### <span data-ttu-id="19c1a-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="19c1a-138">-Slot</span></span>
<span data-ttu-id="19c1a-139">A módosítani kívánt központi verzió környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="19c1a-139">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="19c1a-140">Az érvényes értékek a termelés vagy a megállóhelyek.</span><span class="sxs-lookup"><span data-stu-id="19c1a-140">Valid values are Production or Staging.</span></span>

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

### <span data-ttu-id="19c1a-141">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="19c1a-141">-UninstallConfiguration</span></span>
<span data-ttu-id="19c1a-142">Azt jelzi, hogy ez a parancsmag eltávolítja a felhőalapú szolgáltatásból az összes konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="19c1a-142">Indicates that this cmdlet uninstalls all configurations from the cloud service.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAllRoles
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c1a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c1a-143">CommonParameters</span></span>
<span data-ttu-id="19c1a-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19c1a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c1a-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19c1a-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c1a-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19c1a-146">INPUTS</span></span>

## <span data-ttu-id="19c1a-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19c1a-147">OUTPUTS</span></span>

## <span data-ttu-id="19c1a-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19c1a-148">NOTES</span></span>

## <span data-ttu-id="19c1a-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19c1a-149">RELATED LINKS</span></span>

[<span data-ttu-id="19c1a-150">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="19c1a-150">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="19c1a-151">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="19c1a-151">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


