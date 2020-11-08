---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F8E64309-7AF6-4439-841E-922B11C072AA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 15dd195b86e70ad0a95484417d8cf87b0e544920
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015756"
---
# <span data-ttu-id="48a83-101">Set-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="48a83-101">Set-AzureNetworkSecurityGroupConfig</span></span>

## <span data-ttu-id="48a83-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48a83-102">SYNOPSIS</span></span>

## <span data-ttu-id="48a83-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48a83-103">SYNTAX</span></span>

```
Set-AzureNetworkSecurityGroupConfig [-NetworkSecurityGroupName] <String> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="48a83-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="48a83-104">DESCRIPTION</span></span>

## <span data-ttu-id="48a83-105">Példák</span><span class="sxs-lookup"><span data-stu-id="48a83-105">EXAMPLES</span></span>

### <span data-ttu-id="48a83-106">1:</span><span class="sxs-lookup"><span data-stu-id="48a83-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="48a83-107">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48a83-107">PARAMETERS</span></span>

### <span data-ttu-id="48a83-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="48a83-108">-InformationAction</span></span>
<span data-ttu-id="48a83-109">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="48a83-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="48a83-110">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="48a83-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="48a83-111">Folytassa</span><span class="sxs-lookup"><span data-stu-id="48a83-111">Continue</span></span>
- <span data-ttu-id="48a83-112">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="48a83-112">Ignore</span></span>
- <span data-ttu-id="48a83-113">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="48a83-113">Inquire</span></span>
- <span data-ttu-id="48a83-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="48a83-114">SilentlyContinue</span></span>
- <span data-ttu-id="48a83-115">állj</span><span class="sxs-lookup"><span data-stu-id="48a83-115">Stop</span></span>
- <span data-ttu-id="48a83-116">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="48a83-116">Suspend</span></span>

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

### <span data-ttu-id="48a83-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="48a83-117">-InformationVariable</span></span>
<span data-ttu-id="48a83-118">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="48a83-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="48a83-119">-NetworkSecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="48a83-119">-NetworkSecurityGroupName</span></span>
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

### <span data-ttu-id="48a83-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="48a83-120">-Profile</span></span>
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

### <span data-ttu-id="48a83-121">-VM</span><span class="sxs-lookup"><span data-stu-id="48a83-121">-VM</span></span>
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

### <span data-ttu-id="48a83-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48a83-122">CommonParameters</span></span>
<span data-ttu-id="48a83-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48a83-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48a83-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48a83-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48a83-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48a83-125">INPUTS</span></span>

## <span data-ttu-id="48a83-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48a83-126">OUTPUTS</span></span>

## <span data-ttu-id="48a83-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48a83-127">NOTES</span></span>

## <span data-ttu-id="48a83-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48a83-128">RELATED LINKS</span></span>

[<span data-ttu-id="48a83-129">Remove-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="48a83-129">Remove-AzureNetworkSecurityGroupConfig</span></span>](./Remove-AzureNetworkSecurityGroupConfig.md)


