---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 86438393-8D5A-46A0-B467-6A4434E18011
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42c8760dee1aa095086d4fad3309a3a5da64b296
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016309"
---
# <span data-ttu-id="0e1cf-101">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="0e1cf-101">Get-AzureService</span></span>

## <span data-ttu-id="0e1cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0e1cf-102">SYNOPSIS</span></span>
<span data-ttu-id="0e1cf-103">Egy olyan objektumot ad eredményül, amely információkat nyújt az aktuális előfizetéshez tartozó felhőalapú szolgáltatásokról.</span><span class="sxs-lookup"><span data-stu-id="0e1cf-103">Returns an object with information about the cloud services for the current subscription.</span></span>

## <span data-ttu-id="0e1cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0e1cf-104">SYNTAX</span></span>

```
Get-AzureService [[-ServiceName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0e1cf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0e1cf-105">DESCRIPTION</span></span>
<span data-ttu-id="0e1cf-106">A **Get-AzureService** parancsmag olyan lista-objektumot ad eredményül, amely az aktuális előfizetéshez társított összes Azure Cloud-szolgáltatással rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="0e1cf-106">The **Get-AzureService** cmdlet returns a list object with all of the Azure cloud services associated with the current subscription.</span></span>
<span data-ttu-id="0e1cf-107">Ha a *szolgáltatásnév* paramétert adja meg, a **Get-AzureService** csak a megfelelő szolgáltatás adatait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="0e1cf-107">If you specify the *ServiceName* parameter, **Get-AzureService** returns information on only the matching service.</span></span>

## <span data-ttu-id="0e1cf-108">Példák</span><span class="sxs-lookup"><span data-stu-id="0e1cf-108">EXAMPLES</span></span>

### <span data-ttu-id="0e1cf-109">1. példa: információk kérése az összes szolgáltatásról</span><span class="sxs-lookup"><span data-stu-id="0e1cf-109">Example 1: Get information about all services</span></span>
```
PS C:\> Get-AzureService
```

<span data-ttu-id="0e1cf-110">Ez a parancs olyan objektumot ad eredményül, amely információkat tartalmaz az aktuális előfizetéshez társított összes Azure-szolgáltatásról.</span><span class="sxs-lookup"><span data-stu-id="0e1cf-110">This command returns an object that contains information about all of the Azure services associated with the current subscription.</span></span>

### <span data-ttu-id="0e1cf-111">2. példa: információ kérése adott szolgáltatásról</span><span class="sxs-lookup"><span data-stu-id="0e1cf-111">Example 2: Get information about a specified service</span></span>
```
PS C:\> Get-AzureService -ServiceName $MySvc
```

<span data-ttu-id="0e1cf-112">Ez a parancs információt ad az $MySvc szolgáltatásról.</span><span class="sxs-lookup"><span data-stu-id="0e1cf-112">This command returns information about the $MySvc service.</span></span>

### <span data-ttu-id="0e1cf-113">3. példa: elérhető metódusok és tulajdonságok megjelenítése</span><span class="sxs-lookup"><span data-stu-id="0e1cf-113">Example 3: Display available methods and properties</span></span>
```
PS C:\> Get-AzureService | Get-Member
```

<span data-ttu-id="0e1cf-114">Ez a parancs a **Get-AzureService** parancsmagban elérhető tulajdonságokat és metódusokat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="0e1cf-114">This command displays the properties and methods that are available from the **Get-AzureService** cmdlet.</span></span>

## <span data-ttu-id="0e1cf-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0e1cf-115">PARAMETERS</span></span>

### <span data-ttu-id="0e1cf-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0e1cf-116">-InformationAction</span></span>
<span data-ttu-id="0e1cf-117">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="0e1cf-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0e1cf-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0e1cf-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0e1cf-119">Folytassa</span><span class="sxs-lookup"><span data-stu-id="0e1cf-119">Continue</span></span>
- <span data-ttu-id="0e1cf-120">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="0e1cf-120">Ignore</span></span>
- <span data-ttu-id="0e1cf-121">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="0e1cf-121">Inquire</span></span>
- <span data-ttu-id="0e1cf-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0e1cf-122">SilentlyContinue</span></span>
- <span data-ttu-id="0e1cf-123">állj</span><span class="sxs-lookup"><span data-stu-id="0e1cf-123">Stop</span></span>
- <span data-ttu-id="0e1cf-124">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="0e1cf-124">Suspend</span></span>

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

### <span data-ttu-id="0e1cf-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0e1cf-125">-InformationVariable</span></span>
<span data-ttu-id="0e1cf-126">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="0e1cf-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0e1cf-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="0e1cf-127">-Profile</span></span>
<span data-ttu-id="0e1cf-128">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="0e1cf-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0e1cf-129">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="0e1cf-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0e1cf-130">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="0e1cf-130">-ServiceName</span></span>
<span data-ttu-id="0e1cf-131">Annak a szolgáltatásnak a nevét adja meg, amelyből adatokat szeretne visszaadni.</span><span class="sxs-lookup"><span data-stu-id="0e1cf-131">Specifies the name of a service on which to return information.</span></span>

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

### <span data-ttu-id="0e1cf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e1cf-132">CommonParameters</span></span>
<span data-ttu-id="0e1cf-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0e1cf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e1cf-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e1cf-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e1cf-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e1cf-135">INPUTS</span></span>

## <span data-ttu-id="0e1cf-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e1cf-136">OUTPUTS</span></span>

### <span data-ttu-id="0e1cf-137">HostedServiceContext</span><span class="sxs-lookup"><span data-stu-id="0e1cf-137">HostedServiceContext</span></span>

## <span data-ttu-id="0e1cf-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0e1cf-138">NOTES</span></span>

## <span data-ttu-id="0e1cf-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e1cf-139">RELATED LINKS</span></span>

[<span data-ttu-id="0e1cf-140">Új – AzureService</span><span class="sxs-lookup"><span data-stu-id="0e1cf-140">New-AzureService</span></span>](./New-AzureService.md)

[<span data-ttu-id="0e1cf-141">Set-AzureService</span><span class="sxs-lookup"><span data-stu-id="0e1cf-141">Set-AzureService</span></span>](./Set-AzureService.md)


