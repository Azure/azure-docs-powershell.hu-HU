---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 846B9EB8-8EC2-4BDA-90EF-59098696F460
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c4e1dedb02286ceaab182e0912198c23ec03ee5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015793"
---
# <span data-ttu-id="b1030-101">Set-AzureVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="b1030-101">Set-AzureVMBootDiagnostics</span></span>

## <span data-ttu-id="b1030-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b1030-102">SYNOPSIS</span></span>

## <span data-ttu-id="b1030-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b1030-103">SYNTAX</span></span>

### <span data-ttu-id="b1030-104">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="b1030-104">EnableBootDiagnostics</span></span>
```
Set-AzureVMBootDiagnostics [-Enable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b1030-105">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="b1030-105">DisableBootDiagnostics</span></span>
```
Set-AzureVMBootDiagnostics [-Disable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b1030-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="b1030-106">DESCRIPTION</span></span>

## <span data-ttu-id="b1030-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b1030-107">EXAMPLES</span></span>

### <span data-ttu-id="b1030-108">1:</span><span class="sxs-lookup"><span data-stu-id="b1030-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="b1030-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b1030-109">PARAMETERS</span></span>

### <span data-ttu-id="b1030-110">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="b1030-110">-Disable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1030-111">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="b1030-111">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1030-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b1030-112">-InformationAction</span></span>
<span data-ttu-id="b1030-113">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="b1030-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b1030-114">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b1030-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b1030-115">Folytassa</span><span class="sxs-lookup"><span data-stu-id="b1030-115">Continue</span></span>
- <span data-ttu-id="b1030-116">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="b1030-116">Ignore</span></span>
- <span data-ttu-id="b1030-117">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="b1030-117">Inquire</span></span>
- <span data-ttu-id="b1030-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b1030-118">SilentlyContinue</span></span>
- <span data-ttu-id="b1030-119">állj</span><span class="sxs-lookup"><span data-stu-id="b1030-119">Stop</span></span>
- <span data-ttu-id="b1030-120">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="b1030-120">Suspend</span></span>

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

### <span data-ttu-id="b1030-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b1030-121">-InformationVariable</span></span>
<span data-ttu-id="b1030-122">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="b1030-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b1030-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="b1030-123">-Profile</span></span>
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

### <span data-ttu-id="b1030-124">-VM</span><span class="sxs-lookup"><span data-stu-id="b1030-124">-VM</span></span>
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

### <span data-ttu-id="b1030-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1030-125">CommonParameters</span></span>
<span data-ttu-id="b1030-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b1030-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1030-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1030-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1030-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1030-128">INPUTS</span></span>

## <span data-ttu-id="b1030-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1030-129">OUTPUTS</span></span>

## <span data-ttu-id="b1030-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b1030-130">NOTES</span></span>

## <span data-ttu-id="b1030-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1030-131">RELATED LINKS</span></span>

