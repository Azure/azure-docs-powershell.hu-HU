---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 734C98C1-0EF7-43E5-AB6F-A1C625FF9CE7
online version: ''
schema: 2.0.0
ms.openlocfilehash: f9713c8b39fa4e2842cdf1cfcbfe962ead86d729
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015535"
---
# <span data-ttu-id="d35a9-101">Get-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d35a9-101">Get-AzureVMAccessExtension</span></span>

## <span data-ttu-id="d35a9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d35a9-102">SYNOPSIS</span></span>
<span data-ttu-id="d35a9-103">Az VMAccess-bővítményt egy virtuális gépen alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="d35a9-103">Gets the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="d35a9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d35a9-104">SYNTAX</span></span>

```
Get-AzureVMAccessExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d35a9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d35a9-105">DESCRIPTION</span></span>
<span data-ttu-id="d35a9-106">A **Get-AzureVMAccessExtension** parancsmag a virtuális gépen alkalmazott VMAccess-bővítményt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d35a9-106">The **Get-AzureVMAccessExtension** cmdlet gets the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="d35a9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d35a9-107">EXAMPLES</span></span>

### <span data-ttu-id="d35a9-108">Példa 1: a VMAccess-bővítmény beszerzése virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="d35a9-108">Example 1: Get the VMAccess extension for a virtual machine</span></span>
```
PS C:\> Get-AzureVMAccessExtension -VM $VM;
```

<span data-ttu-id="d35a9-109">Ez a parancs egy virtuális gép VMAccess-bővítményét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d35a9-109">This command gets the VMAccess extension for a virtual machine.</span></span>

## <span data-ttu-id="d35a9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d35a9-110">PARAMETERS</span></span>

### <span data-ttu-id="d35a9-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d35a9-111">-InformationAction</span></span>
<span data-ttu-id="d35a9-112">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="d35a9-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d35a9-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d35a9-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d35a9-114">Folytassa</span><span class="sxs-lookup"><span data-stu-id="d35a9-114">Continue</span></span>
- <span data-ttu-id="d35a9-115">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="d35a9-115">Ignore</span></span>
- <span data-ttu-id="d35a9-116">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="d35a9-116">Inquire</span></span>
- <span data-ttu-id="d35a9-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d35a9-117">SilentlyContinue</span></span>
- <span data-ttu-id="d35a9-118">állj</span><span class="sxs-lookup"><span data-stu-id="d35a9-118">Stop</span></span>
- <span data-ttu-id="d35a9-119">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="d35a9-119">Suspend</span></span>

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

### <span data-ttu-id="d35a9-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d35a9-120">-InformationVariable</span></span>
<span data-ttu-id="d35a9-121">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="d35a9-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d35a9-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="d35a9-122">-Profile</span></span>
<span data-ttu-id="d35a9-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d35a9-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d35a9-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d35a9-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d35a9-125">-VM</span><span class="sxs-lookup"><span data-stu-id="d35a9-125">-VM</span></span>
<span data-ttu-id="d35a9-126">Az állandó virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d35a9-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="d35a9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d35a9-127">CommonParameters</span></span>
<span data-ttu-id="d35a9-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d35a9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d35a9-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d35a9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d35a9-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d35a9-130">INPUTS</span></span>

## <span data-ttu-id="d35a9-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d35a9-131">OUTPUTS</span></span>

## <span data-ttu-id="d35a9-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d35a9-132">NOTES</span></span>

## <span data-ttu-id="d35a9-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d35a9-133">RELATED LINKS</span></span>

[<span data-ttu-id="d35a9-134">Remove-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d35a9-134">Remove-AzureVMAccessExtension</span></span>](./Remove-AzureVMAccessExtension.md)

[<span data-ttu-id="d35a9-135">Set-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d35a9-135">Set-AzureVMAccessExtension</span></span>](./Set-AzureVMAccessExtension.md)


