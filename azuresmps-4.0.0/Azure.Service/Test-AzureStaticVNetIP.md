---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4E059EF1-740C-4AEB-AF41-BF6003BE15F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: a52f2585771ec10d6acf52b14c88bd1ed0af0427
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015936"
---
# <span data-ttu-id="ff309-101">Test-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="ff309-101">Test-AzureStaticVNetIP</span></span>

## <span data-ttu-id="ff309-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ff309-102">SYNOPSIS</span></span>
<span data-ttu-id="ff309-103">Teszteli a statikus virtuális hálózati IP-cím elérhetőségét, és felsorolja a javaslatokat, ha a lekérdezett cím nem érhető el.</span><span class="sxs-lookup"><span data-stu-id="ff309-103">Tests the availability of a static virtual network IP address, and gets a list of suggestions if the queried address is not available.</span></span>

## <span data-ttu-id="ff309-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ff309-104">SYNTAX</span></span>

```
Test-AzureStaticVNetIP [-VNetName] <String> [-IPAddress] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ff309-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ff309-105">DESCRIPTION</span></span>
<span data-ttu-id="ff309-106">A **AzureStaticVNetIP** parancsmag teszteli a statikus virtuális hálózati IP-cím elérhetőségét, és a javaslatok listáját kapja, ha a lekérdezett cím nem érhető el.</span><span class="sxs-lookup"><span data-stu-id="ff309-106">The **Test-AzureStaticVNetIP** cmdlet tests the availability of a static virtual network IP address, and gets a list of suggestions if the queried address is not available.</span></span>

## <span data-ttu-id="ff309-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ff309-107">EXAMPLES</span></span>

### <span data-ttu-id="ff309-108">1:</span><span class="sxs-lookup"><span data-stu-id="ff309-108">1:</span></span>
```

```

## <span data-ttu-id="ff309-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ff309-109">PARAMETERS</span></span>

### <span data-ttu-id="ff309-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ff309-110">-InformationAction</span></span>
<span data-ttu-id="ff309-111">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="ff309-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ff309-112">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ff309-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ff309-113">Folytassa</span><span class="sxs-lookup"><span data-stu-id="ff309-113">Continue</span></span>
- <span data-ttu-id="ff309-114">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="ff309-114">Ignore</span></span>
- <span data-ttu-id="ff309-115">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="ff309-115">Inquire</span></span>
- <span data-ttu-id="ff309-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ff309-116">SilentlyContinue</span></span>
- <span data-ttu-id="ff309-117">állj</span><span class="sxs-lookup"><span data-stu-id="ff309-117">Stop</span></span>
- <span data-ttu-id="ff309-118">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="ff309-118">Suspend</span></span>

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

### <span data-ttu-id="ff309-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ff309-119">-InformationVariable</span></span>
<span data-ttu-id="ff309-120">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="ff309-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ff309-121">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="ff309-121">-IPAddress</span></span>
<span data-ttu-id="ff309-122">A lekérdezéshez a statikus virtuális IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff309-122">Specifies the static virtual network IP address to query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff309-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="ff309-123">-Profile</span></span>
<span data-ttu-id="ff309-124">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="ff309-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ff309-125">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="ff309-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ff309-126">-VNetName</span><span class="sxs-lookup"><span data-stu-id="ff309-126">-VNetName</span></span>
<span data-ttu-id="ff309-127">A virtuális hálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff309-127">Specifies the Name of the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff309-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff309-128">CommonParameters</span></span>
<span data-ttu-id="ff309-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ff309-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff309-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff309-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff309-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff309-131">INPUTS</span></span>

## <span data-ttu-id="ff309-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff309-132">OUTPUTS</span></span>

## <span data-ttu-id="ff309-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ff309-133">NOTES</span></span>

## <span data-ttu-id="ff309-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff309-134">RELATED LINKS</span></span>

[<span data-ttu-id="ff309-135">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="ff309-135">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="ff309-136">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="ff309-136">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


