---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EE96AC92-02A8-4A40-A26D-0882673E51A5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2dca85290564217f5c4c319ef3531d4c31500fcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016584"
---
# <span data-ttu-id="ab6ac-101">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="ab6ac-101">Get-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="ab6ac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab6ac-102">SYNOPSIS</span></span>

## <span data-ttu-id="ab6ac-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab6ac-103">SYNTAX</span></span>

```
Get-AzureNetworkInterfaceConfig [[-Name] <String>] -VM <PersistentVMRoleContext>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ab6ac-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab6ac-104">DESCRIPTION</span></span>

## <span data-ttu-id="ab6ac-105">Példák</span><span class="sxs-lookup"><span data-stu-id="ab6ac-105">EXAMPLES</span></span>

### <span data-ttu-id="ab6ac-106">1:</span><span class="sxs-lookup"><span data-stu-id="ab6ac-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="ab6ac-107">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab6ac-107">PARAMETERS</span></span>

### <span data-ttu-id="ab6ac-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ab6ac-108">-InformationAction</span></span>
<span data-ttu-id="ab6ac-109">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="ab6ac-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ab6ac-110">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ab6ac-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ab6ac-111">Folytassa</span><span class="sxs-lookup"><span data-stu-id="ab6ac-111">Continue</span></span>
- <span data-ttu-id="ab6ac-112">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="ab6ac-112">Ignore</span></span>
- <span data-ttu-id="ab6ac-113">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="ab6ac-113">Inquire</span></span>
- <span data-ttu-id="ab6ac-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ab6ac-114">SilentlyContinue</span></span>
- <span data-ttu-id="ab6ac-115">állj</span><span class="sxs-lookup"><span data-stu-id="ab6ac-115">Stop</span></span>
- <span data-ttu-id="ab6ac-116">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="ab6ac-116">Suspend</span></span>

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

### <span data-ttu-id="ab6ac-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ab6ac-117">-InformationVariable</span></span>
<span data-ttu-id="ab6ac-118">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="ab6ac-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ab6ac-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ab6ac-119">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab6ac-120">-VM</span><span class="sxs-lookup"><span data-stu-id="ab6ac-120">-VM</span></span>
```yaml
Type: PersistentVMRoleContext
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab6ac-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab6ac-121">CommonParameters</span></span>
<span data-ttu-id="ab6ac-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab6ac-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab6ac-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab6ac-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab6ac-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab6ac-124">INPUTS</span></span>

## <span data-ttu-id="ab6ac-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab6ac-125">OUTPUTS</span></span>

## <span data-ttu-id="ab6ac-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab6ac-126">NOTES</span></span>

## <span data-ttu-id="ab6ac-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab6ac-127">RELATED LINKS</span></span>

[<span data-ttu-id="ab6ac-128">Add-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="ab6ac-128">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="ab6ac-129">Remove-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="ab6ac-129">Remove-AzureNetworkInterfaceConfig</span></span>](./Remove-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="ab6ac-130">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="ab6ac-130">Set-AzureNetworkInterfaceConfig</span></span>](./Set-AzureNetworkInterfaceConfig.md)


