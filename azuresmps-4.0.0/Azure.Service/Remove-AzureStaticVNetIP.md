---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 94D20309-5F72-4BE5-A150-2D6DD754286A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a9d793bb9bc8d96150b812474bed9f8997adbe1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016104"
---
# <span data-ttu-id="435ce-101">Remove-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="435ce-101">Remove-AzureStaticVNetIP</span></span>

## <span data-ttu-id="435ce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="435ce-102">SYNOPSIS</span></span>
<span data-ttu-id="435ce-103">Eltávolítja a statikus virtuális hálózati IP-cím adatait egy virtuálisgép-objektumból (ha van ilyen).</span><span class="sxs-lookup"><span data-stu-id="435ce-103">Removes the static virtual network IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="435ce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="435ce-104">SYNTAX</span></span>

```
Remove-AzureStaticVNetIP -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="435ce-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="435ce-105">DESCRIPTION</span></span>
<span data-ttu-id="435ce-106">A **Remove-AzureStaticVNetIP** parancsmag eltávolítja a statikus virtuális hálózat (VNet) IP-címét egy virtuálisgép-objektumból (ha van ilyen).</span><span class="sxs-lookup"><span data-stu-id="435ce-106">The **Remove-AzureStaticVNetIP** cmdlet removes the static virtual network (VNet) IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="435ce-107">Példák</span><span class="sxs-lookup"><span data-stu-id="435ce-107">EXAMPLES</span></span>

### <span data-ttu-id="435ce-108">1:</span><span class="sxs-lookup"><span data-stu-id="435ce-108">1:</span></span>
```

```

## <span data-ttu-id="435ce-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="435ce-109">PARAMETERS</span></span>

### <span data-ttu-id="435ce-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="435ce-110">-InformationAction</span></span>
<span data-ttu-id="435ce-111">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="435ce-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="435ce-112">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="435ce-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="435ce-113">Folytassa</span><span class="sxs-lookup"><span data-stu-id="435ce-113">Continue</span></span>
- <span data-ttu-id="435ce-114">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="435ce-114">Ignore</span></span>
- <span data-ttu-id="435ce-115">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="435ce-115">Inquire</span></span>
- <span data-ttu-id="435ce-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="435ce-116">SilentlyContinue</span></span>
- <span data-ttu-id="435ce-117">állj</span><span class="sxs-lookup"><span data-stu-id="435ce-117">Stop</span></span>
- <span data-ttu-id="435ce-118">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="435ce-118">Suspend</span></span>

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

### <span data-ttu-id="435ce-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="435ce-119">-InformationVariable</span></span>
<span data-ttu-id="435ce-120">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="435ce-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="435ce-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="435ce-121">-Profile</span></span>
<span data-ttu-id="435ce-122">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="435ce-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="435ce-123">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="435ce-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="435ce-124">-VM</span><span class="sxs-lookup"><span data-stu-id="435ce-124">-VM</span></span>
<span data-ttu-id="435ce-125">Állandó virtuálisgép-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="435ce-125">Specifies a persistent virtual machine object.</span></span>

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

### <span data-ttu-id="435ce-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="435ce-126">CommonParameters</span></span>
<span data-ttu-id="435ce-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="435ce-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="435ce-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="435ce-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="435ce-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="435ce-129">INPUTS</span></span>

## <span data-ttu-id="435ce-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="435ce-130">OUTPUTS</span></span>

## <span data-ttu-id="435ce-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="435ce-131">NOTES</span></span>

## <span data-ttu-id="435ce-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="435ce-132">RELATED LINKS</span></span>

[<span data-ttu-id="435ce-133">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="435ce-133">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="435ce-134">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="435ce-134">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


