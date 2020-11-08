---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 377716B6-8B8C-4CAE-A8FA-835DA24F04C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9610c6b8abaf4d59d6a363253d0b90a0dfcecad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016043"
---
# <span data-ttu-id="5b327-101">Set-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="5b327-101">Set-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="5b327-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5b327-102">SYNOPSIS</span></span>
<span data-ttu-id="5b327-103">Egy virtuális gép BGInfo-bővítményének beállítása.</span><span class="sxs-lookup"><span data-stu-id="5b327-103">Sets the BGInfo extension for a virtual machine.</span></span>

## <span data-ttu-id="5b327-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5b327-104">SYNTAX</span></span>

### <span data-ttu-id="5b327-105">SetBGInfoExtension (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5b327-105">SetBGInfoExtension (Default)</span></span>
```
Set-AzureVMBGInfoExtension [-Disable] [[-ReferenceName] <String>] [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b327-106">UninstallBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="5b327-106">UninstallBGInfoExtension</span></span>
```
Set-AzureVMBGInfoExtension [-Uninstall] [[-ReferenceName] <String>] [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b327-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5b327-107">DESCRIPTION</span></span>
<span data-ttu-id="5b327-108">A **set-AzureVMBGInfoExtension** parancsmag a virtuális gép BGInfo bővítményét állítja be.</span><span class="sxs-lookup"><span data-stu-id="5b327-108">The **Set-AzureVMBGInfoExtension** cmdlet sets the BGInfo extension for a virtual machine.</span></span>

## <span data-ttu-id="5b327-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5b327-109">EXAMPLES</span></span>

### <span data-ttu-id="5b327-110">1. példa: a BGInfo-bővítmény beállítása virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="5b327-110">Example 1: Set the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMBGInfoExtension -VM $VM
```

<span data-ttu-id="5b327-111">Ez a parancs a megadott virtuális gép BGInfo-bővítményét állítja be a $VM változóban tárolt módon.</span><span class="sxs-lookup"><span data-stu-id="5b327-111">This command sets the BGInfo extension for the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="5b327-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5b327-112">PARAMETERS</span></span>

### <span data-ttu-id="5b327-113">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="5b327-113">-Disable</span></span>
<span data-ttu-id="5b327-114">Jelzi, hogy ez a parancsmag letiltja a bővítmény állapotát.</span><span class="sxs-lookup"><span data-stu-id="5b327-114">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetBGInfoExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b327-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5b327-115">-InformationAction</span></span>
<span data-ttu-id="5b327-116">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="5b327-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5b327-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="5b327-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5b327-118">Folytassa</span><span class="sxs-lookup"><span data-stu-id="5b327-118">Continue</span></span>
- <span data-ttu-id="5b327-119">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="5b327-119">Ignore</span></span>
- <span data-ttu-id="5b327-120">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="5b327-120">Inquire</span></span>
- <span data-ttu-id="5b327-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5b327-121">SilentlyContinue</span></span>
- <span data-ttu-id="5b327-122">állj</span><span class="sxs-lookup"><span data-stu-id="5b327-122">Stop</span></span>
- <span data-ttu-id="5b327-123">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="5b327-123">Suspend</span></span>

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

### <span data-ttu-id="5b327-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5b327-124">-InformationVariable</span></span>
<span data-ttu-id="5b327-125">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="5b327-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5b327-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="5b327-126">-Profile</span></span>
<span data-ttu-id="5b327-127">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="5b327-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5b327-128">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="5b327-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5b327-129">-Hivatkozásnév</span><span class="sxs-lookup"><span data-stu-id="5b327-129">-ReferenceName</span></span>
<span data-ttu-id="5b327-130">Az BGInfo-bővítmény hivatkozási nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b327-130">Specifies the reference name of the BGInfo extension.</span></span>

<span data-ttu-id="5b327-131">Ez a paraméter egy felhasználó által definiált karakterlánc, amellyel hivatkozhat a bővítményekre.</span><span class="sxs-lookup"><span data-stu-id="5b327-131">This parameter is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="5b327-132">A program akkor adja meg, ha a bővítményt első alkalommal felveszi a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="5b327-132">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="5b327-133">A kiterjesztés frissítésekor megadhatja a korábban használt hivatkozási nevet is.</span><span class="sxs-lookup"><span data-stu-id="5b327-133">You can specify the previously used reference name while updating the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b327-134">-Uninstall</span><span class="sxs-lookup"><span data-stu-id="5b327-134">-Uninstall</span></span>
<span data-ttu-id="5b327-135">Azt jelzi, hogy ez a parancsmag eltávolítja a BGInfo-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="5b327-135">Indicates that this cmdlet uninstalls the BGInfo extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallBGInfoExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b327-136">-Verzió</span><span class="sxs-lookup"><span data-stu-id="5b327-136">-Version</span></span>
<span data-ttu-id="5b327-137">Az BGInfo-bővítmény verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b327-137">Specifies the version of the BGInfo extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b327-138">-VM</span><span class="sxs-lookup"><span data-stu-id="5b327-138">-VM</span></span>
<span data-ttu-id="5b327-139">Az állandó virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b327-139">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="5b327-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b327-140">CommonParameters</span></span>
<span data-ttu-id="5b327-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5b327-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b327-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b327-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b327-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b327-143">INPUTS</span></span>

## <span data-ttu-id="5b327-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b327-144">OUTPUTS</span></span>

## <span data-ttu-id="5b327-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5b327-145">NOTES</span></span>

## <span data-ttu-id="5b327-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b327-146">RELATED LINKS</span></span>

[<span data-ttu-id="5b327-147">Get-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="5b327-147">Get-AzureVMBGInfoExtension</span></span>](./Get-AzureVMBGInfoExtension.md)

[<span data-ttu-id="5b327-148">Remove-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="5b327-148">Remove-AzureVMBGInfoExtension</span></span>](./Remove-AzureVMBGInfoExtension.md)


