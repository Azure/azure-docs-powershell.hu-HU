---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 185C2680-501F-497D-81B2-5F6E30A91F16
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55e9f6f026e7e524613a0e070767bc2ab26f6d66
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016466"
---
# <span data-ttu-id="d2640-101">Remove-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="d2640-101">Remove-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="d2640-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d2640-102">SYNOPSIS</span></span>

## <span data-ttu-id="d2640-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d2640-103">SYNTAX</span></span>

```
Remove-AzureNetworkInterfaceConfig [-Name] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d2640-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="d2640-104">DESCRIPTION</span></span>

## <span data-ttu-id="d2640-105">Példák</span><span class="sxs-lookup"><span data-stu-id="d2640-105">EXAMPLES</span></span>

### <span data-ttu-id="d2640-106">1:</span><span class="sxs-lookup"><span data-stu-id="d2640-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="d2640-107">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d2640-107">PARAMETERS</span></span>

### <span data-ttu-id="d2640-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d2640-108">-InformationAction</span></span>
<span data-ttu-id="d2640-109">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="d2640-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d2640-110">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d2640-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d2640-111">Folytassa</span><span class="sxs-lookup"><span data-stu-id="d2640-111">Continue</span></span>
- <span data-ttu-id="d2640-112">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="d2640-112">Ignore</span></span>
- <span data-ttu-id="d2640-113">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="d2640-113">Inquire</span></span>
- <span data-ttu-id="d2640-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d2640-114">SilentlyContinue</span></span>
- <span data-ttu-id="d2640-115">állj</span><span class="sxs-lookup"><span data-stu-id="d2640-115">Stop</span></span>
- <span data-ttu-id="d2640-116">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="d2640-116">Suspend</span></span>

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

### <span data-ttu-id="d2640-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d2640-117">-InformationVariable</span></span>
<span data-ttu-id="d2640-118">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="d2640-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d2640-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d2640-119">-Name</span></span>
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

### <span data-ttu-id="d2640-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="d2640-120">-Profile</span></span>
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

### <span data-ttu-id="d2640-121">-VM</span><span class="sxs-lookup"><span data-stu-id="d2640-121">-VM</span></span>
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

### <span data-ttu-id="d2640-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2640-122">CommonParameters</span></span>
<span data-ttu-id="d2640-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d2640-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2640-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2640-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2640-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2640-125">INPUTS</span></span>

## <span data-ttu-id="d2640-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2640-126">OUTPUTS</span></span>

## <span data-ttu-id="d2640-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d2640-127">NOTES</span></span>

## <span data-ttu-id="d2640-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2640-128">RELATED LINKS</span></span>

[<span data-ttu-id="d2640-129">Add-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="d2640-129">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="d2640-130">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="d2640-130">Get-AzureNetworkInterfaceConfig</span></span>](./Get-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="d2640-131">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="d2640-131">Set-AzureNetworkInterfaceConfig</span></span>](./Set-AzureNetworkInterfaceConfig.md)


