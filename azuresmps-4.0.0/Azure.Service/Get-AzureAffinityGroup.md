---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 77B26360-F22B-457F-BDE3-9920A5736947
online version: ''
schema: 2.0.0
ms.openlocfilehash: 323b04a57cffc71059dff3f91480d54684941695
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015671"
---
# <span data-ttu-id="89c81-101">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="89c81-101">Get-AzureAffinityGroup</span></span>

## <span data-ttu-id="89c81-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="89c81-102">SYNOPSIS</span></span>
<span data-ttu-id="89c81-103">Azure affinitású csoport objektumát kapja.</span><span class="sxs-lookup"><span data-stu-id="89c81-103">Gets an Azure affinity group object.</span></span>

## <span data-ttu-id="89c81-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="89c81-104">SYNTAX</span></span>

```
Get-AzureAffinityGroup [[-Name] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="89c81-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="89c81-105">DESCRIPTION</span></span>
<span data-ttu-id="89c81-106">A **Get-AzureAffinityGroup** parancsmag az Azure affinitás csoportba kerül.</span><span class="sxs-lookup"><span data-stu-id="89c81-106">The **Get-AzureAffinityGroup** cmdlet gets an Azure affinity group.</span></span>
<span data-ttu-id="89c81-107">Az affinitás csoport objektuma magában foglalja az affinitás csoport nevét, a helyet, a címkét, a leírást, valamint az affinitás csoport részét képező tárolási és hosztolt szolgáltatásokat.</span><span class="sxs-lookup"><span data-stu-id="89c81-107">The affinity group object includes the affinity group name, location, label, description and the storage and hosted services that are part of the affinity group.</span></span>

## <span data-ttu-id="89c81-108">Példák</span><span class="sxs-lookup"><span data-stu-id="89c81-108">EXAMPLES</span></span>

### <span data-ttu-id="89c81-109">Példa 1: az affinitás csoport tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="89c81-109">Example 1: Get properties of an affinity group</span></span>
```
PS C:\> Get-AzureAffinityGroup -Name "South01"
```

<span data-ttu-id="89c81-110">Ez a parancs a South01 nevű affinitás csoport tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="89c81-110">This command gets the properties of the affinity group named South01.</span></span>

## <span data-ttu-id="89c81-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="89c81-111">PARAMETERS</span></span>

### <span data-ttu-id="89c81-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="89c81-112">-InformationAction</span></span>
<span data-ttu-id="89c81-113">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="89c81-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="89c81-114">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="89c81-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="89c81-115">Folytassa</span><span class="sxs-lookup"><span data-stu-id="89c81-115">Continue</span></span>
- <span data-ttu-id="89c81-116">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="89c81-116">Ignore</span></span>
- <span data-ttu-id="89c81-117">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="89c81-117">Inquire</span></span>
- <span data-ttu-id="89c81-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="89c81-118">SilentlyContinue</span></span>
- <span data-ttu-id="89c81-119">állj</span><span class="sxs-lookup"><span data-stu-id="89c81-119">Stop</span></span>
- <span data-ttu-id="89c81-120">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="89c81-120">Suspend</span></span>

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

### <span data-ttu-id="89c81-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="89c81-121">-InformationVariable</span></span>
<span data-ttu-id="89c81-122">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="89c81-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="89c81-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="89c81-123">-Name</span></span>
<span data-ttu-id="89c81-124">Itt adhatja meg annak a affinitásnak a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="89c81-124">Specifies the name of the affinity group that this cmdlet gets.</span></span>
<span data-ttu-id="89c81-125">A felügyeleti portálon létrehozott affinitási csoportok nevei jellemzően GUID-nek számítanak.</span><span class="sxs-lookup"><span data-stu-id="89c81-125">Names for affinity groups created through the Management Portal are typically GUIDs.</span></span>
<span data-ttu-id="89c81-126">A kezelési port az affinitás csoport címkéjét jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="89c81-126">The Management Port shows the affinity group label.</span></span>

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

### <span data-ttu-id="89c81-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="89c81-127">-Profile</span></span>
<span data-ttu-id="89c81-128">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="89c81-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="89c81-129">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="89c81-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="89c81-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89c81-130">CommonParameters</span></span>
<span data-ttu-id="89c81-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="89c81-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89c81-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89c81-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89c81-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="89c81-133">INPUTS</span></span>

## <span data-ttu-id="89c81-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89c81-134">OUTPUTS</span></span>

### <span data-ttu-id="89c81-135">AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="89c81-135">AffinityGroup</span></span>

## <span data-ttu-id="89c81-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="89c81-136">NOTES</span></span>

## <span data-ttu-id="89c81-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89c81-137">RELATED LINKS</span></span>

[<span data-ttu-id="89c81-138">Új – AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="89c81-138">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="89c81-139">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="89c81-139">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)

[<span data-ttu-id="89c81-140">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="89c81-140">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


