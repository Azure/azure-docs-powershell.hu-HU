---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 93A8B8EC-4ED0-4C87-AF92-9A246ECEF4F0
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1b516722b0555c84400c0c8f5acd7f1b5c43d9c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015510"
---
# <span data-ttu-id="6ba63-101">Remove-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="6ba63-101">Remove-AzureVMAccessExtension</span></span>

## <span data-ttu-id="6ba63-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6ba63-102">SYNOPSIS</span></span>
<span data-ttu-id="6ba63-103">Eltávolítja a virtuális gépen alkalmazott VMAccess-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="6ba63-103">Removes the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="6ba63-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6ba63-104">SYNTAX</span></span>

```
Remove-AzureVMAccessExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6ba63-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6ba63-105">DESCRIPTION</span></span>
<span data-ttu-id="6ba63-106">A **Remove-AzureVMAccessExtension** parancsmag eltávolítja a virtuális gépen alkalmazott VMAccess-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="6ba63-106">The **Remove-AzureVMAccessExtension** cmdlet removes the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="6ba63-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6ba63-107">EXAMPLES</span></span>

### <span data-ttu-id="6ba63-108">1. példa: VMAccess-bővítmény eltávolítása virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="6ba63-108">Example 1: Remove a VMAccess extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMAccessExtension -VM $VM;
```

<span data-ttu-id="6ba63-109">Ez a parancs eltávolítja a VMAccess-bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="6ba63-109">This command removes a VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="6ba63-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6ba63-110">PARAMETERS</span></span>

### <span data-ttu-id="6ba63-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6ba63-111">-InformationAction</span></span>
<span data-ttu-id="6ba63-112">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="6ba63-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6ba63-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="6ba63-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6ba63-114">Folytassa</span><span class="sxs-lookup"><span data-stu-id="6ba63-114">Continue</span></span>
- <span data-ttu-id="6ba63-115">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="6ba63-115">Ignore</span></span>
- <span data-ttu-id="6ba63-116">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="6ba63-116">Inquire</span></span>
- <span data-ttu-id="6ba63-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6ba63-117">SilentlyContinue</span></span>
- <span data-ttu-id="6ba63-118">állj</span><span class="sxs-lookup"><span data-stu-id="6ba63-118">Stop</span></span>
- <span data-ttu-id="6ba63-119">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="6ba63-119">Suspend</span></span>

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

### <span data-ttu-id="6ba63-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6ba63-120">-InformationVariable</span></span>
<span data-ttu-id="6ba63-121">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="6ba63-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6ba63-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="6ba63-122">-Profile</span></span>
<span data-ttu-id="6ba63-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="6ba63-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6ba63-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="6ba63-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6ba63-125">-VM</span><span class="sxs-lookup"><span data-stu-id="6ba63-125">-VM</span></span>
<span data-ttu-id="6ba63-126">Annak a virtuális számítógép-objektumnak a meghatározása, amelyre a parancsmag eltávolítja a VMAccess-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="6ba63-126">Specifies the persistent virtual machine object that this cmdlet removes the VMAccess extension from.</span></span>

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

### <span data-ttu-id="6ba63-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ba63-127">CommonParameters</span></span>
<span data-ttu-id="6ba63-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6ba63-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ba63-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ba63-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ba63-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ba63-130">INPUTS</span></span>

## <span data-ttu-id="6ba63-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ba63-131">OUTPUTS</span></span>

## <span data-ttu-id="6ba63-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6ba63-132">NOTES</span></span>

## <span data-ttu-id="6ba63-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ba63-133">RELATED LINKS</span></span>

[<span data-ttu-id="6ba63-134">Get-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="6ba63-134">Get-AzureVMAccessExtension</span></span>](./Get-AzureVMAccessExtension.md)

[<span data-ttu-id="6ba63-135">Set-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="6ba63-135">Set-AzureVMAccessExtension</span></span>](./Set-AzureVMAccessExtension.md)


