---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9AAEDD44-D11E-47A3-BF0F-D8445A018759
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46dbd7ec58cc112e6573fa3d9c6a52fe0ee14b33
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016443"
---
# <span data-ttu-id="01153-101">Remove-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="01153-101">Remove-AzureVMPuppetExtension</span></span>

## <span data-ttu-id="01153-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="01153-102">SYNOPSIS</span></span>
<span data-ttu-id="01153-103">Eltávolítja a virtuális gépen alkalmazott báb-kiterjesztést.</span><span class="sxs-lookup"><span data-stu-id="01153-103">Removes the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="01153-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="01153-104">SYNTAX</span></span>

```
Remove-AzureVMPuppetExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="01153-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="01153-105">DESCRIPTION</span></span>
<span data-ttu-id="01153-106">A **Remove-AzureVMPuppetExtension** parancsmag eltávolítja a virtuális gépen alkalmazott báb-kiterjesztést.</span><span class="sxs-lookup"><span data-stu-id="01153-106">The **Remove-AzureVMPuppetExtension** cmdlet removes the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="01153-107">Példák</span><span class="sxs-lookup"><span data-stu-id="01153-107">EXAMPLES</span></span>

### <span data-ttu-id="01153-108">Példa 1: a virtuális gépen alkalmazott báb-kiterjesztés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="01153-108">Example 1: Remove the Puppet extension applied on a virtual machine</span></span>
```
PS C:\> Remove-AzureVMPuppetExtension -VM $VM;
```

<span data-ttu-id="01153-109">Ez a parancs eltávolítja a megadott virtuális gépen alkalmazott báb-kiterjesztést.</span><span class="sxs-lookup"><span data-stu-id="01153-109">This command removes the Puppet extension applied on the specified virtual machine.</span></span>

## <span data-ttu-id="01153-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="01153-110">PARAMETERS</span></span>

### <span data-ttu-id="01153-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="01153-111">-InformationAction</span></span>
<span data-ttu-id="01153-112">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="01153-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="01153-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="01153-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="01153-114">Folytassa</span><span class="sxs-lookup"><span data-stu-id="01153-114">Continue</span></span>
- <span data-ttu-id="01153-115">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="01153-115">Ignore</span></span>
- <span data-ttu-id="01153-116">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="01153-116">Inquire</span></span>
- <span data-ttu-id="01153-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="01153-117">SilentlyContinue</span></span>
- <span data-ttu-id="01153-118">állj</span><span class="sxs-lookup"><span data-stu-id="01153-118">Stop</span></span>
- <span data-ttu-id="01153-119">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="01153-119">Suspend</span></span>

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

### <span data-ttu-id="01153-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="01153-120">-InformationVariable</span></span>
<span data-ttu-id="01153-121">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="01153-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="01153-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="01153-122">-Profile</span></span>
<span data-ttu-id="01153-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="01153-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="01153-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="01153-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="01153-125">-VM</span><span class="sxs-lookup"><span data-stu-id="01153-125">-VM</span></span>
<span data-ttu-id="01153-126">Az állandó virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="01153-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="01153-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01153-127">CommonParameters</span></span>
<span data-ttu-id="01153-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="01153-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01153-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01153-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01153-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="01153-130">INPUTS</span></span>

## <span data-ttu-id="01153-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01153-131">OUTPUTS</span></span>

## <span data-ttu-id="01153-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="01153-132">NOTES</span></span>

## <span data-ttu-id="01153-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01153-133">RELATED LINKS</span></span>

[<span data-ttu-id="01153-134">Get-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="01153-134">Get-AzureVMPuppetExtension</span></span>](./Get-AzureVMPuppetExtension.md)

[<span data-ttu-id="01153-135">Set-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="01153-135">Set-AzureVMPuppetExtension</span></span>](./Set-AzureVMPuppetExtension.md)


