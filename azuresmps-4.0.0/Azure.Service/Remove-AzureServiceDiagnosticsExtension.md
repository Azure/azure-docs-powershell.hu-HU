---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95298AFC-B492-4EA6-AFC2-E862D3086AF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84b1256d7d911d22a4f1344bdf841943ce87ee7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016116"
---
# <span data-ttu-id="dd89f-101">Remove-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="dd89f-101">Remove-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="dd89f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd89f-102">SYNOPSIS</span></span>
<span data-ttu-id="dd89f-103">Eltávolítja a felhőalapú szolgáltatás diagnosztikai bővítményét az összes szerepkörön vagy elnevezett szerepkörökön egy bizonyos terjesztési bővítőhelyen.</span><span class="sxs-lookup"><span data-stu-id="dd89f-103">Removes the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="dd89f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd89f-104">SYNTAX</span></span>

### <span data-ttu-id="dd89f-105">RemoveByRoles (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dd89f-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd89f-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="dd89f-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [-UninstallConfiguration]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd89f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd89f-107">DESCRIPTION</span></span>
<span data-ttu-id="dd89f-108">A **Remove-AzureServiceDiagnosticsExtension** parancsmag eltávolítja a felhőalapú szolgáltatás diagnosztikai bővítményét az összes szerepkörben vagy elnevezett szerepkörökben egy bizonyos terjesztési bővítőhelyen.</span><span class="sxs-lookup"><span data-stu-id="dd89f-108">The **Remove-AzureServiceDiagnosticsExtension** cmdlet removes the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="dd89f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="dd89f-109">EXAMPLES</span></span>

### <span data-ttu-id="dd89f-110">1. példa: egy szolgáltatás diagnosztikai bővítményének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dd89f-110">Example 1: Remove the diagnostic extension for a service</span></span>
```
PS C:\> Remove-AzureServiceDiagnosticsExtension -ServiceName $Svc
```

<span data-ttu-id="dd89f-111">Ez a parancs eltávolítja a meghatározott szerepkör diagnosztikai bővítményét.</span><span class="sxs-lookup"><span data-stu-id="dd89f-111">This command removes the diagnostic extension for a specified role.</span></span>

### <span data-ttu-id="dd89f-112">2. példa: egy szolgáltatás diagnosztikai bővítményének eltávolítása meghatározott szerepkörben</span><span class="sxs-lookup"><span data-stu-id="dd89f-112">Example 2: Remove the diagnostic extension for a service in a specified role</span></span>
```
PS C:\> Remove-AzureServiceDiagnosticsExtension -ServiceName $Svc -Role "WebRole01"
```

<span data-ttu-id="dd89f-113">Ez a parancs eltávolítja a meghatározott szerepkör diagnosztikai bővítményét.</span><span class="sxs-lookup"><span data-stu-id="dd89f-113">This command removes the diagnostic extension for a specified role.</span></span>

## <span data-ttu-id="dd89f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd89f-114">PARAMETERS</span></span>

### <span data-ttu-id="dd89f-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="dd89f-115">-InformationAction</span></span>
<span data-ttu-id="dd89f-116">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="dd89f-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="dd89f-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="dd89f-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dd89f-118">Folytassa</span><span class="sxs-lookup"><span data-stu-id="dd89f-118">Continue</span></span>
- <span data-ttu-id="dd89f-119">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="dd89f-119">Ignore</span></span>
- <span data-ttu-id="dd89f-120">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="dd89f-120">Inquire</span></span>
- <span data-ttu-id="dd89f-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="dd89f-121">SilentlyContinue</span></span>
- <span data-ttu-id="dd89f-122">állj</span><span class="sxs-lookup"><span data-stu-id="dd89f-122">Stop</span></span>
- <span data-ttu-id="dd89f-123">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="dd89f-123">Suspend</span></span>

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

### <span data-ttu-id="dd89f-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="dd89f-124">-InformationVariable</span></span>
<span data-ttu-id="dd89f-125">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="dd89f-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="dd89f-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="dd89f-126">-Profile</span></span>
<span data-ttu-id="dd89f-127">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="dd89f-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dd89f-128">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="dd89f-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dd89f-129">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="dd89f-129">-Role</span></span>
<span data-ttu-id="dd89f-130">Azt a választható szerepköröket adja meg, amelyekhez a távoli asztali konfigurációt meg szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="dd89f-130">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="dd89f-131">Ha nem adja meg ezt a paramétert, a program az összes szerepkör alapértelmezett konfigurációjának megfelelően alkalmazza a távoli asztali konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="dd89f-131">If you do not specify this parameter, the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="dd89f-132">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="dd89f-132">-ServiceName</span></span>
<span data-ttu-id="dd89f-133">A központi üzembe helyezés Azure-szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd89f-133">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="dd89f-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="dd89f-134">-Slot</span></span>
<span data-ttu-id="dd89f-135">A módosítani kívánt központi verzió környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd89f-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="dd89f-136">Az érvényes értékek a termelés vagy a megállóhelyek.</span><span class="sxs-lookup"><span data-stu-id="dd89f-136">Valid values are Production or Staging.</span></span>

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

### <span data-ttu-id="dd89f-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd89f-137">-UninstallConfiguration</span></span>
<span data-ttu-id="dd89f-138">Azt jelzi, hogy ez a parancsmag eltávolítja a felhőalapú szolgáltatásból az összes RDP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="dd89f-138">Indicates that this cmdlet uninstalls all RDP configurations from the cloud service.</span></span>

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

### <span data-ttu-id="dd89f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd89f-139">CommonParameters</span></span>
<span data-ttu-id="dd89f-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd89f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd89f-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd89f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd89f-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd89f-142">INPUTS</span></span>

## <span data-ttu-id="dd89f-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd89f-143">OUTPUTS</span></span>

## <span data-ttu-id="dd89f-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd89f-144">NOTES</span></span>

## <span data-ttu-id="dd89f-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd89f-145">RELATED LINKS</span></span>

[<span data-ttu-id="dd89f-146">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="dd89f-146">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="dd89f-147">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="dd89f-147">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


