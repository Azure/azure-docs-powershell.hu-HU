---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F956CC89-A2CA-4D73-8014-C36778C51927
online version: ''
schema: 2.0.0
ms.openlocfilehash: eba992b183795d016108419834c38bcf64a82d41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016168"
---
# <span data-ttu-id="be6ba-101">Remove-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="be6ba-101">Remove-AzureAvailabilitySet</span></span>

## <span data-ttu-id="be6ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="be6ba-102">SYNOPSIS</span></span>
<span data-ttu-id="be6ba-103">Egy Azure virtuális gépről származó elérhetőségi készlet eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="be6ba-103">Removes an availability set from an Azure virtual machine.</span></span>

## <span data-ttu-id="be6ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="be6ba-104">SYNTAX</span></span>

```
Remove-AzureAvailabilitySet -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="be6ba-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="be6ba-105">DESCRIPTION</span></span>
<span data-ttu-id="be6ba-106">A **Remove-AzureAvailabilitySet** parancsmag eltávolítja a rendelkezésre álló elérhetőségi készletet egy Azure Virtual Machine-ből.</span><span class="sxs-lookup"><span data-stu-id="be6ba-106">The **Remove-AzureAvailabilitySet** cmdlet removes an availability set from an Azure virtual machine.</span></span>

## <span data-ttu-id="be6ba-107">Példák</span><span class="sxs-lookup"><span data-stu-id="be6ba-107">EXAMPLES</span></span>

### <span data-ttu-id="be6ba-108">1:</span><span class="sxs-lookup"><span data-stu-id="be6ba-108">1:</span></span>
```

```

## <span data-ttu-id="be6ba-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="be6ba-109">PARAMETERS</span></span>

### <span data-ttu-id="be6ba-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="be6ba-110">-InformationAction</span></span>
<span data-ttu-id="be6ba-111">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="be6ba-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="be6ba-112">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="be6ba-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="be6ba-113">Folytassa</span><span class="sxs-lookup"><span data-stu-id="be6ba-113">Continue</span></span>
- <span data-ttu-id="be6ba-114">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="be6ba-114">Ignore</span></span>
- <span data-ttu-id="be6ba-115">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="be6ba-115">Inquire</span></span>
- <span data-ttu-id="be6ba-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="be6ba-116">SilentlyContinue</span></span>
- <span data-ttu-id="be6ba-117">állj</span><span class="sxs-lookup"><span data-stu-id="be6ba-117">Stop</span></span>
- <span data-ttu-id="be6ba-118">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="be6ba-118">Suspend</span></span>

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

### <span data-ttu-id="be6ba-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="be6ba-119">-InformationVariable</span></span>
<span data-ttu-id="be6ba-120">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="be6ba-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="be6ba-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="be6ba-121">-Profile</span></span>
<span data-ttu-id="be6ba-122">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="be6ba-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="be6ba-123">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="be6ba-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="be6ba-124">-VM</span><span class="sxs-lookup"><span data-stu-id="be6ba-124">-VM</span></span>
<span data-ttu-id="be6ba-125">Azt a virtuális gépet adja meg, amelyből a parancsmag eltávolítja az elérhetőségi készletet.</span><span class="sxs-lookup"><span data-stu-id="be6ba-125">Specifies the virtual machine from which this cmdlet removes an availability set.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be6ba-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be6ba-126">CommonParameters</span></span>
<span data-ttu-id="be6ba-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="be6ba-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be6ba-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be6ba-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be6ba-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="be6ba-129">INPUTS</span></span>

## <span data-ttu-id="be6ba-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="be6ba-130">OUTPUTS</span></span>

## <span data-ttu-id="be6ba-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="be6ba-131">NOTES</span></span>

## <span data-ttu-id="be6ba-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="be6ba-132">RELATED LINKS</span></span>

[<span data-ttu-id="be6ba-133">Set-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="be6ba-133">Set-AzureAvailabilitySet</span></span>](./Set-AzureAvailabilitySet.md)


