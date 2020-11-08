---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7ED074F0-1E9E-40C2-A543-D19A49831DD3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f0b8ca9acfe5a62b002944bd44e11acfcd38ec1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016533"
---
# <span data-ttu-id="72b08-101">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="72b08-101">Get-AzureVMExtension</span></span>

## <span data-ttu-id="72b08-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72b08-102">SYNOPSIS</span></span>
<span data-ttu-id="72b08-103">A virtuális gépekre alkalmazott erőforrás-kiterjesztéseket kapja.</span><span class="sxs-lookup"><span data-stu-id="72b08-103">Gets resource extensions applied to virtual machines.</span></span>

## <span data-ttu-id="72b08-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72b08-104">SYNTAX</span></span>

### <span data-ttu-id="72b08-105">ListByReferenceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="72b08-105">ListByReferenceName (Default)</span></span>
```
Get-AzureVMExtension [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="72b08-106">ListByExtensionName</span><span class="sxs-lookup"><span data-stu-id="72b08-106">ListByExtensionName</span></span>
```
Get-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="72b08-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="72b08-107">DESCRIPTION</span></span>
<span data-ttu-id="72b08-108">A **Get-AzureVMExtension** parancsmag a virtuális gépekre alkalmazott erőforrás-kiterjesztéseket kapja.</span><span class="sxs-lookup"><span data-stu-id="72b08-108">The **Get-AzureVMExtension** cmdlet gets resource extensions applied to virtual machines.</span></span>

## <span data-ttu-id="72b08-109">Példák</span><span class="sxs-lookup"><span data-stu-id="72b08-109">EXAMPLES</span></span>

### <span data-ttu-id="72b08-110">Példa 1: a virtuális gépre alkalmazott erőforrás-kiterjesztések beszerzése</span><span class="sxs-lookup"><span data-stu-id="72b08-110">Example 1: Get the resource extensions applied to a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName $SVC -Name $VM | Get-AzureVMExtension;
```

<span data-ttu-id="72b08-111">Ez a parancs a megadott virtuális gépre alkalmazott erőforrás-kiterjesztéseket a változó $VM tárolva kapja meg.</span><span class="sxs-lookup"><span data-stu-id="72b08-111">This command gets the resource extensions applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="72b08-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72b08-112">PARAMETERS</span></span>

### <span data-ttu-id="72b08-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="72b08-113">-ExtensionName</span></span>
<span data-ttu-id="72b08-114">A virtuálisgép-bővítmény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72b08-114">Specifies the virtual machine extension name.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b08-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="72b08-115">-InformationAction</span></span>
<span data-ttu-id="72b08-116">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="72b08-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="72b08-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="72b08-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="72b08-118">Folytassa</span><span class="sxs-lookup"><span data-stu-id="72b08-118">Continue</span></span>
- <span data-ttu-id="72b08-119">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="72b08-119">Ignore</span></span>
- <span data-ttu-id="72b08-120">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="72b08-120">Inquire</span></span>
- <span data-ttu-id="72b08-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="72b08-121">SilentlyContinue</span></span>
- <span data-ttu-id="72b08-122">állj</span><span class="sxs-lookup"><span data-stu-id="72b08-122">Stop</span></span>
- <span data-ttu-id="72b08-123">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="72b08-123">Suspend</span></span>

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

### <span data-ttu-id="72b08-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="72b08-124">-InformationVariable</span></span>
<span data-ttu-id="72b08-125">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="72b08-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="72b08-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="72b08-126">-Profile</span></span>
<span data-ttu-id="72b08-127">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="72b08-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="72b08-128">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="72b08-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="72b08-129">-Publisher</span><span class="sxs-lookup"><span data-stu-id="72b08-129">-Publisher</span></span>
<span data-ttu-id="72b08-130">A bővítmény közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72b08-130">Specifies the publisher of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b08-131">-Hivatkozásnév</span><span class="sxs-lookup"><span data-stu-id="72b08-131">-ReferenceName</span></span>
<span data-ttu-id="72b08-132">A kiterjesztés hivatkozási nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72b08-132">Specifies the reference name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByReferenceName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b08-133">-Verzió</span><span class="sxs-lookup"><span data-stu-id="72b08-133">-Version</span></span>
<span data-ttu-id="72b08-134">A bővítmény verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="72b08-134">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b08-135">-VM</span><span class="sxs-lookup"><span data-stu-id="72b08-135">-VM</span></span>
<span data-ttu-id="72b08-136">Az állandó virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="72b08-136">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="72b08-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72b08-137">CommonParameters</span></span>
<span data-ttu-id="72b08-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72b08-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72b08-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72b08-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72b08-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72b08-140">INPUTS</span></span>

## <span data-ttu-id="72b08-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72b08-141">OUTPUTS</span></span>

## <span data-ttu-id="72b08-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72b08-142">NOTES</span></span>

## <span data-ttu-id="72b08-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72b08-143">RELATED LINKS</span></span>

[<span data-ttu-id="72b08-144">Remove-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="72b08-144">Remove-AzureVMExtension</span></span>](./Remove-AzureVMExtension.md)

[<span data-ttu-id="72b08-145">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="72b08-145">Set-AzureVMExtension</span></span>](./Set-AzureVMExtension.md)


