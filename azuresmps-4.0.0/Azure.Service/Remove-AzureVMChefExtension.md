---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A46832F2-CA94-43A4-AFF9-70D02851713F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1146cee245693c19b333af5a4efd9fcc1bebc725
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015505"
---
# <span data-ttu-id="eb421-101">Remove-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="eb421-101">Remove-AzureVMChefExtension</span></span>

## <span data-ttu-id="eb421-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb421-102">SYNOPSIS</span></span>
<span data-ttu-id="eb421-103">Eltávolítja a virtuális gépen alkalmazott séf-kiterjesztést.</span><span class="sxs-lookup"><span data-stu-id="eb421-103">Removes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="eb421-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb421-104">SYNTAX</span></span>

```
Remove-AzureVMChefExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="eb421-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb421-105">DESCRIPTION</span></span>
<span data-ttu-id="eb421-106">A **Remove-AzureVMChefExtension** parancsmag törli a virtuális gépen alkalmazott séf-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="eb421-106">The **Remove-AzureVMChefExtension** cmdlet deletes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="eb421-107">Példák</span><span class="sxs-lookup"><span data-stu-id="eb421-107">EXAMPLES</span></span>

### <span data-ttu-id="eb421-108">1. példa: a kijelölt virtuális gépen alkalmazott Chef-kiterjesztés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="eb421-108">Example 1: Remove the Chef extension applied on the specified virtual machine</span></span>
```
PS C:\> Remove-AzureVMChefExtension -VM $VM;
```

<span data-ttu-id="eb421-109">Ez a parancs eltávolítja a virtuális gépen alkalmazott szakács-kiterjesztést.</span><span class="sxs-lookup"><span data-stu-id="eb421-109">This command removes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="eb421-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb421-110">PARAMETERS</span></span>

### <span data-ttu-id="eb421-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="eb421-111">-InformationAction</span></span>
<span data-ttu-id="eb421-112">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="eb421-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="eb421-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="eb421-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eb421-114">Folytassa</span><span class="sxs-lookup"><span data-stu-id="eb421-114">Continue</span></span>
- <span data-ttu-id="eb421-115">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="eb421-115">Ignore</span></span>
- <span data-ttu-id="eb421-116">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="eb421-116">Inquire</span></span>
- <span data-ttu-id="eb421-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="eb421-117">SilentlyContinue</span></span>
- <span data-ttu-id="eb421-118">állj</span><span class="sxs-lookup"><span data-stu-id="eb421-118">Stop</span></span>
- <span data-ttu-id="eb421-119">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="eb421-119">Suspend</span></span>

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

### <span data-ttu-id="eb421-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="eb421-120">-InformationVariable</span></span>
<span data-ttu-id="eb421-121">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="eb421-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="eb421-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="eb421-122">-Profile</span></span>
<span data-ttu-id="eb421-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="eb421-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="eb421-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="eb421-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="eb421-125">-VM</span><span class="sxs-lookup"><span data-stu-id="eb421-125">-VM</span></span>
<span data-ttu-id="eb421-126">Az állandó virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb421-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="eb421-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb421-127">CommonParameters</span></span>
<span data-ttu-id="eb421-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb421-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb421-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb421-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb421-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb421-130">INPUTS</span></span>

## <span data-ttu-id="eb421-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb421-131">OUTPUTS</span></span>

## <span data-ttu-id="eb421-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb421-132">NOTES</span></span>

## <span data-ttu-id="eb421-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb421-133">RELATED LINKS</span></span>

[<span data-ttu-id="eb421-134">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="eb421-134">Get-AzureVMChefExtension</span></span>](./Get-AzureVMChefExtension.md)

[<span data-ttu-id="eb421-135">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="eb421-135">Set-AzureVMChefExtension</span></span>](./Set-AzureVMChefExtension.md)


