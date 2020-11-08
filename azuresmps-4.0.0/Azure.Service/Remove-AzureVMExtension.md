---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B98FCF46-A5D6-4CC9-B82A-60B429A21A8B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8079844a931debee5b9338e98d405697cc4336f2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015501"
---
# <span data-ttu-id="f2c10-101">Remove-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="f2c10-101">Remove-AzureVMExtension</span></span>

## <span data-ttu-id="f2c10-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f2c10-102">SYNOPSIS</span></span>
<span data-ttu-id="f2c10-103">Eltávolítja az erőforrás-kiterjesztéseket egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="f2c10-103">Removes resource extensions from a virtual machine.</span></span>

## <span data-ttu-id="f2c10-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f2c10-104">SYNTAX</span></span>

### <span data-ttu-id="f2c10-105">RemoveByExtensionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f2c10-105">RemoveByExtensionName (Default)</span></span>
```
Remove-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2c10-106">RemoveByReferenceName</span><span class="sxs-lookup"><span data-stu-id="f2c10-106">RemoveByReferenceName</span></span>
```
Remove-AzureVMExtension [-ReferenceName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f2c10-107">RemoveAll</span><span class="sxs-lookup"><span data-stu-id="f2c10-107">RemoveAll</span></span>
```
Remove-AzureVMExtension [-RemoveAll] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f2c10-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f2c10-108">DESCRIPTION</span></span>
<span data-ttu-id="f2c10-109">A **Remove-AzureVMExtension** parancsmag eltávolítja a virtuális gép erőforrás-bővítményeit.</span><span class="sxs-lookup"><span data-stu-id="f2c10-109">The **Remove-AzureVMExtension** cmdlet removes resource extensions from a virtual machine.</span></span>

## <span data-ttu-id="f2c10-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f2c10-110">EXAMPLES</span></span>

### <span data-ttu-id="f2c10-111">1. példa: kiterjesztés eltávolítása adott névvel és közzétevővel</span><span class="sxs-lookup"><span data-stu-id="f2c10-111">Example 1: Remove an extension using a specific name and publisher</span></span>
```
PS C:\> $VM = Remove-AzureVMExtension -VM $VM -ExtensionName $EXT -Publisher $PUB;
```

<span data-ttu-id="f2c10-112">A parancs eltávolítja a megadott névvel és közzétevővel a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="f2c10-112">This command removes an extension with the specified name and publisher.</span></span>

### <span data-ttu-id="f2c10-113">2. példa: egy adott virtuális gép összes bővítményének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f2c10-113">Example 2: Remove all extensions from a specific virtual machine</span></span>
```
PS C:\> $VM = Remove-AzureVMExtension -VM $VM -RemoveAll;
```

<span data-ttu-id="f2c10-114">Ez a parancs eltávolítja az összes kiterjesztést a megadott virtuális gépről a változó $VM tárolva.</span><span class="sxs-lookup"><span data-stu-id="f2c10-114">This command removes all extensions from the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="f2c10-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f2c10-115">PARAMETERS</span></span>

### <span data-ttu-id="f2c10-116">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="f2c10-116">-ExtensionName</span></span>
<span data-ttu-id="f2c10-117">Megadja a parancsmag által eltávolított kiterjesztés nevét.</span><span class="sxs-lookup"><span data-stu-id="f2c10-117">Specifies the extension name that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByExtensionName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2c10-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f2c10-118">-InformationAction</span></span>
<span data-ttu-id="f2c10-119">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="f2c10-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f2c10-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f2c10-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f2c10-121">Folytassa</span><span class="sxs-lookup"><span data-stu-id="f2c10-121">Continue</span></span>
- <span data-ttu-id="f2c10-122">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="f2c10-122">Ignore</span></span>
- <span data-ttu-id="f2c10-123">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="f2c10-123">Inquire</span></span>
- <span data-ttu-id="f2c10-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f2c10-124">SilentlyContinue</span></span>
- <span data-ttu-id="f2c10-125">állj</span><span class="sxs-lookup"><span data-stu-id="f2c10-125">Stop</span></span>
- <span data-ttu-id="f2c10-126">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="f2c10-126">Suspend</span></span>

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

### <span data-ttu-id="f2c10-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f2c10-127">-InformationVariable</span></span>
<span data-ttu-id="f2c10-128">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="f2c10-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f2c10-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="f2c10-129">-Profile</span></span>
<span data-ttu-id="f2c10-130">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="f2c10-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f2c10-131">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="f2c10-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f2c10-132">-Publisher</span><span class="sxs-lookup"><span data-stu-id="f2c10-132">-Publisher</span></span>
<span data-ttu-id="f2c10-133">A bővítmény közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f2c10-133">Specifies the extension publisher.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByExtensionName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2c10-134">-Hivatkozásnév</span><span class="sxs-lookup"><span data-stu-id="f2c10-134">-ReferenceName</span></span>
<span data-ttu-id="f2c10-135">A kiterjesztés hivatkozási nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f2c10-135">Specifies the reference name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByReferenceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2c10-136">-RemoveAll</span><span class="sxs-lookup"><span data-stu-id="f2c10-136">-RemoveAll</span></span>
<span data-ttu-id="f2c10-137">Azt jelzi, hogy ez a parancsmag eltávolítja a virtuális gépről az összes erőforrás-kiterjesztést.</span><span class="sxs-lookup"><span data-stu-id="f2c10-137">Indicates that this cmdlet removes all resource extensions from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAll
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2c10-138">-VM</span><span class="sxs-lookup"><span data-stu-id="f2c10-138">-VM</span></span>
<span data-ttu-id="f2c10-139">Az állandó virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="f2c10-139">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="f2c10-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2c10-140">CommonParameters</span></span>
<span data-ttu-id="f2c10-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f2c10-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2c10-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2c10-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2c10-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2c10-143">INPUTS</span></span>

## <span data-ttu-id="f2c10-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2c10-144">OUTPUTS</span></span>

## <span data-ttu-id="f2c10-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f2c10-145">NOTES</span></span>

## <span data-ttu-id="f2c10-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2c10-146">RELATED LINKS</span></span>

[<span data-ttu-id="f2c10-147">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="f2c10-147">Get-AzureVMExtension</span></span>](./Get-AzureVMExtension.md)

[<span data-ttu-id="f2c10-148">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="f2c10-148">Set-AzureVMExtension</span></span>](./Set-AzureVMExtension.md)


