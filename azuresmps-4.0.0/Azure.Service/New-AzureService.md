---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BB216903-B2BB-4948-AC28-408ED6C768F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6cae249f99282006ff8636e8d727485a223e2a1d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015899"
---
# <span data-ttu-id="51c59-101">New-AzureService</span><span class="sxs-lookup"><span data-stu-id="51c59-101">New-AzureService</span></span>

## <span data-ttu-id="51c59-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="51c59-102">SYNOPSIS</span></span>
<span data-ttu-id="51c59-103">Azure-szolgáltatást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="51c59-103">Creates an Azure service.</span></span>

## <span data-ttu-id="51c59-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="51c59-104">SYNTAX</span></span>

### <span data-ttu-id="51c59-105">ParameterSetAffinityGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="51c59-105">ParameterSetAffinityGroup (Default)</span></span>
```
New-AzureService [-ServiceName] <String> [-AffinityGroup] <String> [[-Label] <String>]
 [[-Description] <String>] [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="51c59-106">ParameterSetLocation</span><span class="sxs-lookup"><span data-stu-id="51c59-106">ParameterSetLocation</span></span>
```
New-AzureService [-ServiceName] <String> [-Location] <String> [[-Label] <String>] [[-Description] <String>]
 [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="51c59-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="51c59-107">DESCRIPTION</span></span>
<span data-ttu-id="51c59-108">A **New-AzureService** parancsmag új Azure-szolgáltatást hoz létre a jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="51c59-108">The **New-AzureService** cmdlet creates a new Azure service in the current subscription.</span></span>

## <span data-ttu-id="51c59-109">Példák</span><span class="sxs-lookup"><span data-stu-id="51c59-109">EXAMPLES</span></span>

### <span data-ttu-id="51c59-110">Példa 1: szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="51c59-110">Example 1: Create a service</span></span>
```
PS C:\> New-AzureService -ServiceName "MySvc01" -Label "MyTestService" -Location "South Central US"
```

<span data-ttu-id="51c59-111">Ez a parancs létrehoz egy MySvc01 nevű új szolgáltatást a Dél-amerikai Közép-amerikai térségben.</span><span class="sxs-lookup"><span data-stu-id="51c59-111">This command creates a new service named MySvc01 in the South Central US location.</span></span>

### <span data-ttu-id="51c59-112">2. példa: szolgáltatás létrehozása affinitási csoportban</span><span class="sxs-lookup"><span data-stu-id="51c59-112">Example 2: Create a service in an affinity group</span></span>
```
PS C:\> New-AzureService -ServiceName "MySvc01" -AffinityGroup NorthRegion
```

<span data-ttu-id="51c59-113">Ez a parancs létrehoz egy MySvc01 nevű új szolgáltatást a NorthRegion affinitás csoport használatával.</span><span class="sxs-lookup"><span data-stu-id="51c59-113">This command creates a new service named MySvc01 using the NorthRegion affinity group.</span></span>

## <span data-ttu-id="51c59-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="51c59-114">PARAMETERS</span></span>

### <span data-ttu-id="51c59-115">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="51c59-115">-AffinityGroup</span></span>
<span data-ttu-id="51c59-116">Az előfizetéshez társított affinitási csoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="51c59-116">Specifies the affinity group associated with the subscription.</span></span>
<span data-ttu-id="51c59-117">Ha nem adja meg a *hely* paramétert, az affinitás csoport szükséges.</span><span class="sxs-lookup"><span data-stu-id="51c59-117">If you do not specify the *Location* parameter, an affinity group is required.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetAffinityGroup
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51c59-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="51c59-118">-Description</span></span>
<span data-ttu-id="51c59-119">A szolgáltatás leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="51c59-119">Specifies a description for the service.</span></span>
<span data-ttu-id="51c59-120">A Leírás legfeljebb 1024 karakter hosszú lehet.</span><span class="sxs-lookup"><span data-stu-id="51c59-120">The description may be up to 1024 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51c59-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="51c59-121">-InformationAction</span></span>
<span data-ttu-id="51c59-122">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="51c59-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="51c59-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="51c59-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="51c59-124">Folytassa</span><span class="sxs-lookup"><span data-stu-id="51c59-124">Continue</span></span>
- <span data-ttu-id="51c59-125">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="51c59-125">Ignore</span></span>
- <span data-ttu-id="51c59-126">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="51c59-126">Inquire</span></span>
- <span data-ttu-id="51c59-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="51c59-127">SilentlyContinue</span></span>
- <span data-ttu-id="51c59-128">állj</span><span class="sxs-lookup"><span data-stu-id="51c59-128">Stop</span></span>
- <span data-ttu-id="51c59-129">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="51c59-129">Suspend</span></span>

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

### <span data-ttu-id="51c59-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="51c59-130">-InformationVariable</span></span>
<span data-ttu-id="51c59-131">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="51c59-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="51c59-132">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="51c59-132">-Label</span></span>
<span data-ttu-id="51c59-133">A szolgáltatás feliratát adja meg.</span><span class="sxs-lookup"><span data-stu-id="51c59-133">Specifies a label for the service.</span></span>
<span data-ttu-id="51c59-134">Előfordulhat, hogy a címke hossza legfeljebb 100 karakter lehet.</span><span class="sxs-lookup"><span data-stu-id="51c59-134">The label may be up to 100 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51c59-135">-Hely</span><span class="sxs-lookup"><span data-stu-id="51c59-135">-Location</span></span>
<span data-ttu-id="51c59-136">A szolgáltatás helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="51c59-136">Specifies the location for the service.</span></span>
<span data-ttu-id="51c59-137">Ha nincs meghatározott affinitási csoport, a hely szükséges.</span><span class="sxs-lookup"><span data-stu-id="51c59-137">A location is required if there isn't a specified Affinity Group.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetLocation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51c59-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="51c59-138">-Profile</span></span>
<span data-ttu-id="51c59-139">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="51c59-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="51c59-140">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="51c59-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="51c59-141">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="51c59-141">-ReverseDnsFqdn</span></span>
<span data-ttu-id="51c59-142">A DNS-név teljes tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="51c59-142">Specifies the fully qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51c59-143">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="51c59-143">-ServiceName</span></span>
<span data-ttu-id="51c59-144">Az új szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="51c59-144">Specifies the name of the new service.</span></span>
<span data-ttu-id="51c59-145">A névnek egyedinek kell lennie az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="51c59-145">The name must be unique to the subscription.</span></span>

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

### <span data-ttu-id="51c59-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51c59-146">CommonParameters</span></span>
<span data-ttu-id="51c59-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="51c59-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51c59-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51c59-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51c59-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="51c59-149">INPUTS</span></span>

## <span data-ttu-id="51c59-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51c59-150">OUTPUTS</span></span>

## <span data-ttu-id="51c59-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="51c59-151">NOTES</span></span>

## <span data-ttu-id="51c59-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51c59-152">RELATED LINKS</span></span>

[<span data-ttu-id="51c59-153">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="51c59-153">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="51c59-154">Set-AzureService</span><span class="sxs-lookup"><span data-stu-id="51c59-154">Set-AzureService</span></span>](./Set-AzureService.md)


