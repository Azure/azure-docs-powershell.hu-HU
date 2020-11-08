---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 12BF47AA-9E82-425E-A1EB-BAD64D800943
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3be6496993ed6de248103b9a222df4cbe15ed2ff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016557"
---
# <span data-ttu-id="86d55-101">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="86d55-101">Get-AzureStaticVNetIP</span></span>

## <span data-ttu-id="86d55-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86d55-102">SYNOPSIS</span></span>
<span data-ttu-id="86d55-103">A statikus VNet IP-címét egy virtuálisgép-objektumból kapja, ha van ilyen.</span><span class="sxs-lookup"><span data-stu-id="86d55-103">Gets the static VNet IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="86d55-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86d55-104">SYNTAX</span></span>

```
Get-AzureStaticVNetIP -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="86d55-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="86d55-105">DESCRIPTION</span></span>
<span data-ttu-id="86d55-106">A **Get-AzureStaticVNetIP** parancsmag a statikus virtuális hálózat (VNet) IP-címének adatait egy virtuálisgép-objektumból kapja, ha van ilyen.</span><span class="sxs-lookup"><span data-stu-id="86d55-106">The **Get-AzureStaticVNetIP** cmdlet gets the static virtual network (VNet) IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="86d55-107">Példák</span><span class="sxs-lookup"><span data-stu-id="86d55-107">EXAMPLES</span></span>

### <span data-ttu-id="86d55-108">1:</span><span class="sxs-lookup"><span data-stu-id="86d55-108">1:</span></span>
```

```

## <span data-ttu-id="86d55-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86d55-109">PARAMETERS</span></span>

### <span data-ttu-id="86d55-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="86d55-110">-InformationAction</span></span>
<span data-ttu-id="86d55-111">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="86d55-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="86d55-112">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="86d55-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="86d55-113">Folytassa</span><span class="sxs-lookup"><span data-stu-id="86d55-113">Continue</span></span>
- <span data-ttu-id="86d55-114">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="86d55-114">Ignore</span></span>
- <span data-ttu-id="86d55-115">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="86d55-115">Inquire</span></span>
- <span data-ttu-id="86d55-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="86d55-116">SilentlyContinue</span></span>
- <span data-ttu-id="86d55-117">állj</span><span class="sxs-lookup"><span data-stu-id="86d55-117">Stop</span></span>
- <span data-ttu-id="86d55-118">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="86d55-118">Suspend</span></span>

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

### <span data-ttu-id="86d55-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="86d55-119">-InformationVariable</span></span>
<span data-ttu-id="86d55-120">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="86d55-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="86d55-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="86d55-121">-Profile</span></span>
<span data-ttu-id="86d55-122">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="86d55-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="86d55-123">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="86d55-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="86d55-124">-VM</span><span class="sxs-lookup"><span data-stu-id="86d55-124">-VM</span></span>
<span data-ttu-id="86d55-125">Állandó virtuálisgép-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="86d55-125">Specifies a persistent virtual machine object.</span></span>

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

### <span data-ttu-id="86d55-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86d55-126">CommonParameters</span></span>
<span data-ttu-id="86d55-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86d55-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86d55-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86d55-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86d55-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86d55-129">INPUTS</span></span>

## <span data-ttu-id="86d55-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86d55-130">OUTPUTS</span></span>

## <span data-ttu-id="86d55-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86d55-131">NOTES</span></span>

## <span data-ttu-id="86d55-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86d55-132">RELATED LINKS</span></span>

[<span data-ttu-id="86d55-133">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="86d55-133">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


