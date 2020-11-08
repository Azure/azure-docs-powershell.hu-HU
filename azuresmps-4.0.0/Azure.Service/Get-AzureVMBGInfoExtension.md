---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E4CB958B-AC85-4036-A6D6-002FAF40BB66
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5e74be3310b895ef4c941a59541a64f9c6d1b279
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015532"
---
# <span data-ttu-id="e7853-101">Get-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="e7853-101">Get-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="e7853-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e7853-102">SYNOPSIS</span></span>
<span data-ttu-id="e7853-103">Az BGInfo-bővítményt egy virtuális gépen alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="e7853-103">Gets the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="e7853-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e7853-104">SYNTAX</span></span>

```
Get-AzureVMBGInfoExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e7853-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e7853-105">DESCRIPTION</span></span>
<span data-ttu-id="e7853-106">A **Get-AzureVMBGInfoExtension** parancsmag a virtuális gépen alkalmazott BGInfo-bővítményt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e7853-106">The **Get-AzureVMBGInfoExtension** cmdlet gets the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="e7853-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e7853-107">EXAMPLES</span></span>

### <span data-ttu-id="e7853-108">Példa 1: a BGInfo-bővítmény beszerzése adott virtuális gépre</span><span class="sxs-lookup"><span data-stu-id="e7853-108">Example 1: Get the BGInfo extension applied on a specified virtual machine</span></span>
```
PS C:\> Get-AzureVMBGInfoExtension -VM $VM;
```

<span data-ttu-id="e7853-109">Ez a parancs beolvassa a megadott virtuális gépen alkalmazott BGInfo-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="e7853-109">This command gets the BGInfo extension applied on a specified virtual machine</span></span>

## <span data-ttu-id="e7853-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e7853-110">PARAMETERS</span></span>

### <span data-ttu-id="e7853-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e7853-111">-InformationAction</span></span>
<span data-ttu-id="e7853-112">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="e7853-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e7853-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e7853-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e7853-114">Folytassa</span><span class="sxs-lookup"><span data-stu-id="e7853-114">Continue</span></span>
- <span data-ttu-id="e7853-115">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="e7853-115">Ignore</span></span>
- <span data-ttu-id="e7853-116">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="e7853-116">Inquire</span></span>
- <span data-ttu-id="e7853-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e7853-117">SilentlyContinue</span></span>
- <span data-ttu-id="e7853-118">állj</span><span class="sxs-lookup"><span data-stu-id="e7853-118">Stop</span></span>
- <span data-ttu-id="e7853-119">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="e7853-119">Suspend</span></span>

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

### <span data-ttu-id="e7853-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e7853-120">-InformationVariable</span></span>
<span data-ttu-id="e7853-121">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="e7853-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e7853-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="e7853-122">-Profile</span></span>
<span data-ttu-id="e7853-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="e7853-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e7853-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="e7853-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e7853-125">-VM</span><span class="sxs-lookup"><span data-stu-id="e7853-125">-VM</span></span>
<span data-ttu-id="e7853-126">Az állandó virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7853-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="e7853-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7853-127">CommonParameters</span></span>
<span data-ttu-id="e7853-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e7853-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7853-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7853-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7853-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7853-130">INPUTS</span></span>

## <span data-ttu-id="e7853-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7853-131">OUTPUTS</span></span>

## <span data-ttu-id="e7853-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e7853-132">NOTES</span></span>

## <span data-ttu-id="e7853-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7853-133">RELATED LINKS</span></span>

[<span data-ttu-id="e7853-134">Remove-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="e7853-134">Remove-AzureVMBGInfoExtension</span></span>](./Remove-AzureVMBGInfoExtension.md)

[<span data-ttu-id="e7853-135">Set-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="e7853-135">Set-AzureVMBGInfoExtension</span></span>](./Set-AzureVMBGInfoExtension.md)


