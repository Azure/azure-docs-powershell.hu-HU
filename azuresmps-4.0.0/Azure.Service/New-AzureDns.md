---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1085388B-0855-4E29-9043-3FE2C638F58D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22c97045cb5f85256ec4d252cdbfb13c59643008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015924"
---
# <span data-ttu-id="3a57e-101">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="3a57e-101">New-AzureDns</span></span>

## <span data-ttu-id="3a57e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3a57e-102">SYNOPSIS</span></span>
<span data-ttu-id="3a57e-103">Azure DNS Settings-objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="3a57e-103">Creates an Azure DNS settings object.</span></span>

## <span data-ttu-id="3a57e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3a57e-104">SYNTAX</span></span>

```
New-AzureDns [-Name] <String> [-IPAddress] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3a57e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3a57e-105">DESCRIPTION</span></span>
<span data-ttu-id="3a57e-106">A **New-AzureDns** parancsmag egy Azure DNS Settings objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3a57e-106">The **New-AzureDns** cmdlet creates an Azure DNS settings object.</span></span>
<span data-ttu-id="3a57e-107">Ha virtuális gépet hoz létre a **New-AzureVM** parancsmaggal, akkor használhatja a DNS Settings objektumot.</span><span class="sxs-lookup"><span data-stu-id="3a57e-107">You can use a DNS settings object when you create a virtual machine by using the **New-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="3a57e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="3a57e-108">EXAMPLES</span></span>

### <span data-ttu-id="3a57e-109">Példa 1: DNS-beállítások objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="3a57e-109">Example 1: Create a DNS settings object</span></span>
```
PS C:\> $Dns = New-AzureDns -Name "Dns01" -IPAddress "10.1.2.4"
```

<span data-ttu-id="3a57e-110">A parancs Azure DNS Settings objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3a57e-110">This command creates an Azure DNS settings object.</span></span>
<span data-ttu-id="3a57e-111">A DNS-kiszolgáló rendelkezik a megadott címmel és a felhasználóbarát név Dns01.</span><span class="sxs-lookup"><span data-stu-id="3a57e-111">The DNS server has the specified address and the friendly name Dns01.</span></span>
<span data-ttu-id="3a57e-112">A parancs az objektumot a **New-AzureVM** parancsmag által használt $DNS változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3a57e-112">The command stores the object in the $Dns variable for use by the **New-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="3a57e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3a57e-113">PARAMETERS</span></span>

### <span data-ttu-id="3a57e-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3a57e-114">-InformationAction</span></span>
<span data-ttu-id="3a57e-115">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="3a57e-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3a57e-116">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3a57e-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3a57e-117">Folytassa</span><span class="sxs-lookup"><span data-stu-id="3a57e-117">Continue</span></span>
- <span data-ttu-id="3a57e-118">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="3a57e-118">Ignore</span></span>
- <span data-ttu-id="3a57e-119">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="3a57e-119">Inquire</span></span>
- <span data-ttu-id="3a57e-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3a57e-120">SilentlyContinue</span></span>
- <span data-ttu-id="3a57e-121">állj</span><span class="sxs-lookup"><span data-stu-id="3a57e-121">Stop</span></span>
- <span data-ttu-id="3a57e-122">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="3a57e-122">Suspend</span></span>

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

### <span data-ttu-id="3a57e-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3a57e-123">-InformationVariable</span></span>
<span data-ttu-id="3a57e-124">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="3a57e-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3a57e-125">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="3a57e-125">-IPAddress</span></span>
<span data-ttu-id="3a57e-126">A DNS-kiszolgáló IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a57e-126">Specifies the IP address of the DNS server.</span></span>

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

### <span data-ttu-id="3a57e-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3a57e-127">-Name</span></span>
<span data-ttu-id="3a57e-128">A DNS-kiszolgáló felhasználóbarát nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a57e-128">Specifies a friendly name for the DNS server.</span></span>
<span data-ttu-id="3a57e-129">Ez a név nem feltétlenül teljesen minősített tartománynév.</span><span class="sxs-lookup"><span data-stu-id="3a57e-129">This name is not necessarily a fully qualified domain name.</span></span>

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

### <span data-ttu-id="3a57e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a57e-130">CommonParameters</span></span>
<span data-ttu-id="3a57e-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3a57e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a57e-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a57e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a57e-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a57e-133">INPUTS</span></span>

## <span data-ttu-id="3a57e-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a57e-134">OUTPUTS</span></span>

## <span data-ttu-id="3a57e-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3a57e-135">NOTES</span></span>

## <span data-ttu-id="3a57e-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a57e-136">RELATED LINKS</span></span>

[<span data-ttu-id="3a57e-137">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="3a57e-137">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="3a57e-138">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="3a57e-138">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="3a57e-139">Új – AzureVM</span><span class="sxs-lookup"><span data-stu-id="3a57e-139">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="3a57e-140">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="3a57e-140">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="3a57e-141">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="3a57e-141">Set-AzureDns</span></span>](./Set-AzureDns.md)


