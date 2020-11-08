---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A4E88106-1B47-4ACD-8F35-027D16EA7791
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85b3422581fa884245807f258adcc31d52404c53
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015805"
---
# <span data-ttu-id="b018b-101">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="b018b-101">Set-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="b018b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b018b-102">SYNOPSIS</span></span>

## <span data-ttu-id="b018b-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b018b-103">SYNTAX</span></span>

```
Set-AzureNetworkInterfaceConfig [-Name] <String> [-SubnetName] <String> [[-StaticVNetIPAddress] <String>]
 [[-NetworkSecurityGroup] <String>] [[-IPForwarding] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b018b-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="b018b-104">DESCRIPTION</span></span>

## <span data-ttu-id="b018b-105">Példák</span><span class="sxs-lookup"><span data-stu-id="b018b-105">EXAMPLES</span></span>

### <span data-ttu-id="b018b-106">1:</span><span class="sxs-lookup"><span data-stu-id="b018b-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="b018b-107">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b018b-107">PARAMETERS</span></span>

### <span data-ttu-id="b018b-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b018b-108">-InformationAction</span></span>
<span data-ttu-id="b018b-109">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="b018b-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b018b-110">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b018b-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b018b-111">Folytassa</span><span class="sxs-lookup"><span data-stu-id="b018b-111">Continue</span></span>
- <span data-ttu-id="b018b-112">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="b018b-112">Ignore</span></span>
- <span data-ttu-id="b018b-113">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="b018b-113">Inquire</span></span>
- <span data-ttu-id="b018b-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b018b-114">SilentlyContinue</span></span>
- <span data-ttu-id="b018b-115">állj</span><span class="sxs-lookup"><span data-stu-id="b018b-115">Stop</span></span>
- <span data-ttu-id="b018b-116">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="b018b-116">Suspend</span></span>

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

### <span data-ttu-id="b018b-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b018b-117">-InformationVariable</span></span>
<span data-ttu-id="b018b-118">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="b018b-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b018b-119">-IPForwarding</span><span class="sxs-lookup"><span data-stu-id="b018b-119">-IPForwarding</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b018b-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b018b-120">-Name</span></span>
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

### <span data-ttu-id="b018b-121">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b018b-121">-NetworkSecurityGroup</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b018b-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="b018b-122">-Profile</span></span>
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

### <span data-ttu-id="b018b-123">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="b018b-123">-StaticVNetIPAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b018b-124">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="b018b-124">-SubnetName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b018b-125">-VM</span><span class="sxs-lookup"><span data-stu-id="b018b-125">-VM</span></span>
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

### <span data-ttu-id="b018b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b018b-126">CommonParameters</span></span>
<span data-ttu-id="b018b-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b018b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b018b-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b018b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b018b-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b018b-129">INPUTS</span></span>

## <span data-ttu-id="b018b-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b018b-130">OUTPUTS</span></span>

## <span data-ttu-id="b018b-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b018b-131">NOTES</span></span>

## <span data-ttu-id="b018b-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b018b-132">RELATED LINKS</span></span>

[<span data-ttu-id="b018b-133">Add-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="b018b-133">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="b018b-134">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="b018b-134">Get-AzureNetworkInterfaceConfig</span></span>](./Get-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="b018b-135">Remove-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="b018b-135">Remove-AzureNetworkInterfaceConfig</span></span>](./Remove-AzureNetworkInterfaceConfig.md)


