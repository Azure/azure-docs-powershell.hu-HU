---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6A280C0B-5F55-4575-9B11-596F497C4305
online version: ''
schema: 2.0.0
ms.openlocfilehash: 71e49425724926848ee69b24f5dfca70df664913
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016126"
---
# <span data-ttu-id="0ab00-101">Remove-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="0ab00-101">Remove-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="0ab00-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ab00-102">SYNOPSIS</span></span>
<span data-ttu-id="0ab00-103">Eltávolítja a felhőalapú szolgáltatás AD tartományi bővítményét az összes szerepkörön vagy elnevezett szerepkörökön egy bizonyos terjesztési bővítőhelyen.</span><span class="sxs-lookup"><span data-stu-id="0ab00-103">Removes the cloud service AD domain extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="0ab00-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ab00-104">SYNTAX</span></span>

### <span data-ttu-id="0ab00-105">RemoveByRoles (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0ab00-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ab00-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="0ab00-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [-UninstallConfiguration]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ab00-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ab00-107">DESCRIPTION</span></span>
<span data-ttu-id="0ab00-108">A **Remove-AzureServiceADDomainExtension** parancsmag eltávolítja a felhőalapú szolgáltatás Active Directory (ad) tartományi bővítményét az összes szerepkörben vagy elnevezett szerepkörökben egy bizonyos központi telepítő bővítőhelyen.</span><span class="sxs-lookup"><span data-stu-id="0ab00-108">The **Remove-AzureServiceADDomainExtension** cmdlet removes the cloud service Active Directory (AD) domain extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="0ab00-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0ab00-109">EXAMPLES</span></span>

### <span data-ttu-id="0ab00-110">Példa 1: AD domain-bővítmény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0ab00-110">Example 1: Remove an AD domain extension</span></span>
```
PS C:\> Remove-AzureServiceADDomainExtension -ServiceName $Svc
```

<span data-ttu-id="0ab00-111">Ez a parancs eltávolítja a $Svc változó által megadott kiterjesztést.</span><span class="sxs-lookup"><span data-stu-id="0ab00-111">This command removes the extension specified by the $Svc variable.</span></span>

### <span data-ttu-id="0ab00-112">2. példa: adott szerepkörhöz tartozó AD tartományi bővítmény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0ab00-112">Example 2: Remove an AD Domain extension for a specified role</span></span>
```
PS C:\> Remove-AzureServiceADDomainExtension -ServiceName $Svc -Role "WebRole1"
```

<span data-ttu-id="0ab00-113">Ez a parancs eltávolítja a megadott szerepkörhöz tartozó bővítményt.</span><span class="sxs-lookup"><span data-stu-id="0ab00-113">This command removes the service extension for the specified role.</span></span>

## <span data-ttu-id="0ab00-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ab00-114">PARAMETERS</span></span>

### <span data-ttu-id="0ab00-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0ab00-115">-InformationAction</span></span>
<span data-ttu-id="0ab00-116">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="0ab00-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0ab00-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0ab00-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0ab00-118">Folytassa</span><span class="sxs-lookup"><span data-stu-id="0ab00-118">Continue</span></span>
- <span data-ttu-id="0ab00-119">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="0ab00-119">Ignore</span></span>
- <span data-ttu-id="0ab00-120">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="0ab00-120">Inquire</span></span>
- <span data-ttu-id="0ab00-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0ab00-121">SilentlyContinue</span></span>
- <span data-ttu-id="0ab00-122">állj</span><span class="sxs-lookup"><span data-stu-id="0ab00-122">Stop</span></span>
- <span data-ttu-id="0ab00-123">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="0ab00-123">Suspend</span></span>

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

### <span data-ttu-id="0ab00-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0ab00-124">-InformationVariable</span></span>
<span data-ttu-id="0ab00-125">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="0ab00-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0ab00-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="0ab00-126">-Profile</span></span>
<span data-ttu-id="0ab00-127">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="0ab00-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0ab00-128">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="0ab00-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0ab00-129">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="0ab00-129">-Role</span></span>
<span data-ttu-id="0ab00-130">Azt a választható szerepköröket adja meg, amelyekhez a távoli asztali konfigurációt meg szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="0ab00-130">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="0ab00-131">Ha nem adja meg, akkor a rendszer az AD-tartomány konfigurációját alkalmazza alapértelmezett konfigurációként az összes szerepkörben.</span><span class="sxs-lookup"><span data-stu-id="0ab00-131">If not specified, the AD domain configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="0ab00-132">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="0ab00-132">-ServiceName</span></span>
<span data-ttu-id="0ab00-133">Egy Azure-szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ab00-133">Specifies the name of an Azure service.</span></span>

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

### <span data-ttu-id="0ab00-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="0ab00-134">-Slot</span></span>
<span data-ttu-id="0ab00-135">A módosítani kívánt központi verzió környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ab00-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="0ab00-136">Érvényes értékek: a termelés vagy a megállóhely.</span><span class="sxs-lookup"><span data-stu-id="0ab00-136">Valid values are: Production or Staging.</span></span>

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

### <span data-ttu-id="0ab00-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="0ab00-137">-UninstallConfiguration</span></span>
<span data-ttu-id="0ab00-138">Azt jelzi, hogy ez a parancsmag eltávolítja az összes AD-tartomány konfigurációját a felhőalapú szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="0ab00-138">Indicates that this cmdlet uninstalls all AD domain configurations from the cloud service.</span></span>

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

### <span data-ttu-id="0ab00-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ab00-139">CommonParameters</span></span>
<span data-ttu-id="0ab00-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ab00-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ab00-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ab00-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ab00-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ab00-142">INPUTS</span></span>

## <span data-ttu-id="0ab00-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ab00-143">OUTPUTS</span></span>

## <span data-ttu-id="0ab00-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ab00-144">NOTES</span></span>

## <span data-ttu-id="0ab00-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ab00-145">RELATED LINKS</span></span>

[<span data-ttu-id="0ab00-146">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="0ab00-146">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="0ab00-147">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="0ab00-147">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


