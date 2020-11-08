---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1721107D-22FF-4A42-93C6-FD812DF81C33
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac1bb63645b8db9e6a66971ad4ecd3b545a39100
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016545"
---
# <span data-ttu-id="41ef3-101">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="41ef3-101">Get-AzureVMChefExtension</span></span>

## <span data-ttu-id="41ef3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41ef3-102">SYNOPSIS</span></span>
<span data-ttu-id="41ef3-103">A séf által megadott kiterjesztést kapja egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="41ef3-103">Gets the Chef extension applied on a virtual machine.</span></span>

## <span data-ttu-id="41ef3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41ef3-104">SYNTAX</span></span>

```
Get-AzureVMChefExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="41ef3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="41ef3-105">DESCRIPTION</span></span>
<span data-ttu-id="41ef3-106">A **Get-AzureVMChefExtension** parancsmag beilleszti a Chef bővítményt egy virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="41ef3-106">The **Get-AzureVMChefExtension** cmdlet gets the Chef extension applied on a virtual machine.</span></span>

## <span data-ttu-id="41ef3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="41ef3-107">EXAMPLES</span></span>

### <span data-ttu-id="41ef3-108">1. példa: a szakács által megadott bővítmény beszerzése a megadott virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="41ef3-108">Example 1: Get the Chef extension applied on the specified virtual machine</span></span>
```
PS C:\> Get-AzureVMChefExtension -VM $VM;
```

<span data-ttu-id="41ef3-109">Ez a parancs a megadott virtuális gépen a szakács által megadott kiterjesztést kapja.</span><span class="sxs-lookup"><span data-stu-id="41ef3-109">This command gets the Chef extension applied on the specified virtual machine.</span></span>

## <span data-ttu-id="41ef3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41ef3-110">PARAMETERS</span></span>

### <span data-ttu-id="41ef3-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="41ef3-111">-InformationAction</span></span>
<span data-ttu-id="41ef3-112">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="41ef3-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="41ef3-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="41ef3-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="41ef3-114">Folytassa</span><span class="sxs-lookup"><span data-stu-id="41ef3-114">Continue</span></span>
- <span data-ttu-id="41ef3-115">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="41ef3-115">Ignore</span></span>
- <span data-ttu-id="41ef3-116">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="41ef3-116">Inquire</span></span>
- <span data-ttu-id="41ef3-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="41ef3-117">SilentlyContinue</span></span>
- <span data-ttu-id="41ef3-118">állj</span><span class="sxs-lookup"><span data-stu-id="41ef3-118">Stop</span></span>
- <span data-ttu-id="41ef3-119">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="41ef3-119">Suspend</span></span>

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

### <span data-ttu-id="41ef3-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="41ef3-120">-InformationVariable</span></span>
<span data-ttu-id="41ef3-121">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="41ef3-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="41ef3-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="41ef3-122">-Profile</span></span>
<span data-ttu-id="41ef3-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="41ef3-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="41ef3-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="41ef3-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="41ef3-125">-VM</span><span class="sxs-lookup"><span data-stu-id="41ef3-125">-VM</span></span>
<span data-ttu-id="41ef3-126">Az állandó virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="41ef3-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="41ef3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41ef3-127">CommonParameters</span></span>
<span data-ttu-id="41ef3-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41ef3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41ef3-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41ef3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41ef3-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41ef3-130">INPUTS</span></span>

## <span data-ttu-id="41ef3-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41ef3-131">OUTPUTS</span></span>

## <span data-ttu-id="41ef3-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41ef3-132">NOTES</span></span>

## <span data-ttu-id="41ef3-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41ef3-133">RELATED LINKS</span></span>

[<span data-ttu-id="41ef3-134">Remove-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="41ef3-134">Remove-AzureVMChefExtension</span></span>](./Remove-AzureVMChefExtension.md)

[<span data-ttu-id="41ef3-135">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="41ef3-135">Set-AzureVMChefExtension</span></span>](./Set-AzureVMChefExtension.md)


