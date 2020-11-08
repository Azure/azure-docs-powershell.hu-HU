---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9AC28E79-0E3F-4AED-8BFE-8D1C4DCB7715
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd7ece4f8f414df7be6e2d38920f516119f4b82a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016526"
---
# <span data-ttu-id="34c19-101">Get-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="34c19-101">Get-AzureVMPuppetExtension</span></span>

## <span data-ttu-id="34c19-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="34c19-102">SYNOPSIS</span></span>
<span data-ttu-id="34c19-103">A báb-kiterjesztést egy virtuális gépen alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="34c19-103">Gets the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="34c19-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="34c19-104">SYNTAX</span></span>

```
Get-AzureVMPuppetExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="34c19-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="34c19-105">DESCRIPTION</span></span>
<span data-ttu-id="34c19-106">A **Get-AzureVMPuppetExtension** parancsmag a virtuális gépen alkalmazott báb-kiterjesztést kapja.</span><span class="sxs-lookup"><span data-stu-id="34c19-106">The **Get-AzureVMPuppetExtension** cmdlet gets the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="34c19-107">Példák</span><span class="sxs-lookup"><span data-stu-id="34c19-107">EXAMPLES</span></span>

### <span data-ttu-id="34c19-108">1. példa: a báb-kiterjesztés beszerzése virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="34c19-108">Example 1: Get the Puppet extension applied on a virtual machine</span></span>
```
PS C:\> Get-AzureVMPuppetExtension -VM $VM
```

<span data-ttu-id="34c19-109">Ez a parancs a virtuális gépen alkalmazott báb-kiterjesztést kapja.</span><span class="sxs-lookup"><span data-stu-id="34c19-109">This command gets the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="34c19-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="34c19-110">PARAMETERS</span></span>

### <span data-ttu-id="34c19-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="34c19-111">-InformationAction</span></span>
<span data-ttu-id="34c19-112">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="34c19-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="34c19-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="34c19-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="34c19-114">Folytassa</span><span class="sxs-lookup"><span data-stu-id="34c19-114">Continue</span></span>
- <span data-ttu-id="34c19-115">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="34c19-115">Ignore</span></span>
- <span data-ttu-id="34c19-116">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="34c19-116">Inquire</span></span>
- <span data-ttu-id="34c19-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="34c19-117">SilentlyContinue</span></span>
- <span data-ttu-id="34c19-118">állj</span><span class="sxs-lookup"><span data-stu-id="34c19-118">Stop</span></span>
- <span data-ttu-id="34c19-119">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="34c19-119">Suspend</span></span>

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

### <span data-ttu-id="34c19-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="34c19-120">-InformationVariable</span></span>
<span data-ttu-id="34c19-121">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="34c19-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="34c19-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="34c19-122">-Profile</span></span>
<span data-ttu-id="34c19-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="34c19-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="34c19-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="34c19-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="34c19-125">-VM</span><span class="sxs-lookup"><span data-stu-id="34c19-125">-VM</span></span>
<span data-ttu-id="34c19-126">Az állandó virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="34c19-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="34c19-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34c19-127">CommonParameters</span></span>
<span data-ttu-id="34c19-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="34c19-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34c19-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34c19-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34c19-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="34c19-130">INPUTS</span></span>

## <span data-ttu-id="34c19-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="34c19-131">OUTPUTS</span></span>

## <span data-ttu-id="34c19-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="34c19-132">NOTES</span></span>

## <span data-ttu-id="34c19-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="34c19-133">RELATED LINKS</span></span>

[<span data-ttu-id="34c19-134">Remove-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="34c19-134">Remove-AzureVMPuppetExtension</span></span>](./Remove-AzureVMPuppetExtension.md)

[<span data-ttu-id="34c19-135">Set-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="34c19-135">Set-AzureVMPuppetExtension</span></span>](./Set-AzureVMPuppetExtension.md)


