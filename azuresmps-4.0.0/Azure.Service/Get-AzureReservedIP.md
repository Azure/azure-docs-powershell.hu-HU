---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C0EEC51F-F8AB-4A6C-8F99-2B2DFFE9BB26
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9b5f4d5319e705c4f0481edcb5a44a579f4ff01d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015618"
---
# <span data-ttu-id="4f281-101">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="4f281-101">Get-AzureReservedIP</span></span>

## <span data-ttu-id="4f281-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4f281-102">SYNOPSIS</span></span>
<span data-ttu-id="4f281-103">Egy fenntartott IP-címet kap a nevével, vagy felsorolja az előfizetésben lévő összes lefoglalt IP-címet.</span><span class="sxs-lookup"><span data-stu-id="4f281-103">Gets a reserved IP address by its name or lists all the reserved IP addresses in the subscription.</span></span>

## <span data-ttu-id="4f281-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4f281-104">SYNTAX</span></span>

```
Get-AzureReservedIP [[-ReservedIPName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4f281-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4f281-105">DESCRIPTION</span></span>
<span data-ttu-id="4f281-106">A **Get-AzureReservedIP** parancsmag a lefoglalt IP-címet a neve alapján kapja meg, vagy felsorolja az előfizetésben szereplő összes lefoglalt IP-címet.</span><span class="sxs-lookup"><span data-stu-id="4f281-106">The **Get-AzureReservedIP** cmdlet gets a reserved IP address by its name or lists all of the reserved IP addresses in the subscription.</span></span>

## <span data-ttu-id="4f281-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4f281-107">EXAMPLES</span></span>

### <span data-ttu-id="4f281-108">Példa 1: az összes fenntartott IP-cím beolvasása</span><span class="sxs-lookup"><span data-stu-id="4f281-108">Example 1: Get all reserved IP addresses</span></span>
```
PS C:\> Get-AzureReservedIP
```

<span data-ttu-id="4f281-109">Ez a parancs a lefoglalt IP-címeket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4f281-109">This command gets all reserved IP addresses.</span></span>

### <span data-ttu-id="4f281-110">2. példa: fenntartott IP-cím beszerzése megadott névvel</span><span class="sxs-lookup"><span data-stu-id="4f281-110">Example 2: Get a reserved IP address with a specified name</span></span>
```
PS C:\> Get-AzureReservedIP -ReservedIPName $IpName
```

<span data-ttu-id="4f281-111">Ez a parancs azt a fenntartott IP-címet kapja meg, amelynek nevét a $IpName változó adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f281-111">This command gets the reserved IP address that has the name specified by the $IpName variable.</span></span>

## <span data-ttu-id="4f281-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4f281-112">PARAMETERS</span></span>

### <span data-ttu-id="4f281-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4f281-113">-InformationAction</span></span>
<span data-ttu-id="4f281-114">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="4f281-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4f281-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4f281-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4f281-116">Folytassa</span><span class="sxs-lookup"><span data-stu-id="4f281-116">Continue</span></span>
- <span data-ttu-id="4f281-117">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="4f281-117">Ignore</span></span>
- <span data-ttu-id="4f281-118">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="4f281-118">Inquire</span></span>
- <span data-ttu-id="4f281-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4f281-119">SilentlyContinue</span></span>
- <span data-ttu-id="4f281-120">állj</span><span class="sxs-lookup"><span data-stu-id="4f281-120">Stop</span></span>
- <span data-ttu-id="4f281-121">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="4f281-121">Suspend</span></span>

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

### <span data-ttu-id="4f281-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4f281-122">-InformationVariable</span></span>
<span data-ttu-id="4f281-123">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="4f281-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4f281-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="4f281-124">-Profile</span></span>
<span data-ttu-id="4f281-125">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="4f281-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4f281-126">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="4f281-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4f281-127">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="4f281-127">-ReservedIPName</span></span>
<span data-ttu-id="4f281-128">A fenntartott IP-nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f281-128">Specifies the reserved IP name.</span></span>

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

### <span data-ttu-id="4f281-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f281-129">CommonParameters</span></span>
<span data-ttu-id="4f281-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4f281-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f281-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f281-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f281-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f281-132">INPUTS</span></span>

## <span data-ttu-id="4f281-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f281-133">OUTPUTS</span></span>

## <span data-ttu-id="4f281-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4f281-134">NOTES</span></span>

## <span data-ttu-id="4f281-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4f281-135">RELATED LINKS</span></span>

[<span data-ttu-id="4f281-136">Új – AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="4f281-136">New-AzureReservedIP</span></span>](./New-AzureReservedIP.md)

[<span data-ttu-id="4f281-137">Remove-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="4f281-137">Remove-AzureReservedIP</span></span>](./Remove-AzureReservedIP.md)


