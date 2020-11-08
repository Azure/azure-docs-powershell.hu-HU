---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CCA6334F-A193-4506-B873-76F29980C68D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25749aca2d0fb2682404d6c4d006c8ad1b1f3c6b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016336"
---
# <span data-ttu-id="5ef18-101">Get-AzureLocation</span><span class="sxs-lookup"><span data-stu-id="5ef18-101">Get-AzureLocation</span></span>

## <span data-ttu-id="5ef18-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ef18-102">SYNOPSIS</span></span>
<span data-ttu-id="5ef18-103">Az aktuális Azure-előfizetéshez elérhető adatközpont helyeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5ef18-103">Gets the available data center locations for the current Azure subscription.</span></span>

## <span data-ttu-id="5ef18-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ef18-104">SYNTAX</span></span>

```
Get-AzureLocation [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5ef18-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ef18-105">DESCRIPTION</span></span>
<span data-ttu-id="5ef18-106">A **Get-AzureLocation** parancsmag felsorolja az elérhető Azure-adatközpontokat és az aktuális Azure-előfizetéshez tartozó tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="5ef18-106">The **Get-AzureLocation** cmdlet gets a list of the available Azure data centers and their properties for the current Azure subscription.</span></span>
<span data-ttu-id="5ef18-107">A parancsmag futtatása előtt be kell állítania a jelenlegi előfizetést a Select-AzureSubscription és a Set-AzureSubscription parancsmagok segítségével.</span><span class="sxs-lookup"><span data-stu-id="5ef18-107">Before you run this cmdlet, you must set your current subscription by using the Select-AzureSubscription and Set-AzureSubscription cmdlets.</span></span>

## <span data-ttu-id="5ef18-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5ef18-108">EXAMPLES</span></span>

### <span data-ttu-id="5ef18-109">Példa 1: helyek beszerzése</span><span class="sxs-lookup"><span data-stu-id="5ef18-109">Example 1: Get locations</span></span>
```
PS C:\> Get-AzureLocation
```

<span data-ttu-id="5ef18-110">Ez a parancs az aktuális előfizetéshez elérhető adatközpontok és tulajdonságaik listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5ef18-110">This command gets a list of available data centers, and their properties, for the current subscription.</span></span>

## <span data-ttu-id="5ef18-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ef18-111">PARAMETERS</span></span>

### <span data-ttu-id="5ef18-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5ef18-112">-InformationAction</span></span>
<span data-ttu-id="5ef18-113">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="5ef18-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5ef18-114">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="5ef18-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5ef18-115">Folytassa</span><span class="sxs-lookup"><span data-stu-id="5ef18-115">Continue</span></span>
- <span data-ttu-id="5ef18-116">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="5ef18-116">Ignore</span></span>
- <span data-ttu-id="5ef18-117">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="5ef18-117">Inquire</span></span>
- <span data-ttu-id="5ef18-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5ef18-118">SilentlyContinue</span></span>
- <span data-ttu-id="5ef18-119">állj</span><span class="sxs-lookup"><span data-stu-id="5ef18-119">Stop</span></span>
- <span data-ttu-id="5ef18-120">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="5ef18-120">Suspend</span></span>

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

### <span data-ttu-id="5ef18-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5ef18-121">-InformationVariable</span></span>
<span data-ttu-id="5ef18-122">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="5ef18-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5ef18-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="5ef18-123">-Profile</span></span>
<span data-ttu-id="5ef18-124">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="5ef18-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5ef18-125">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="5ef18-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5ef18-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ef18-126">CommonParameters</span></span>
<span data-ttu-id="5ef18-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ef18-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ef18-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ef18-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ef18-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ef18-129">INPUTS</span></span>

## <span data-ttu-id="5ef18-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ef18-130">OUTPUTS</span></span>

## <span data-ttu-id="5ef18-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ef18-131">NOTES</span></span>

## <span data-ttu-id="5ef18-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ef18-132">RELATED LINKS</span></span>

