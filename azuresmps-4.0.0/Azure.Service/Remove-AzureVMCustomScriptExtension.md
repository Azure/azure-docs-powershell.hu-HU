---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3DCA1502-9528-458D-A9EA-762A4BD2726B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284fcf4bd31eeb9437b8cc7669fff0824155180f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016448"
---
# <span data-ttu-id="3340e-101">Remove-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="3340e-101">Remove-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="3340e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3340e-102">SYNOPSIS</span></span>
<span data-ttu-id="3340e-103">Eltávolítja az egyéni parancsfájl-kiterjesztést egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="3340e-103">Removes the custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="3340e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3340e-104">SYNTAX</span></span>

```
Remove-AzureVMCustomScriptExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3340e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3340e-105">DESCRIPTION</span></span>
<span data-ttu-id="3340e-106">A **Remove-AzureVMCustomScriptExtension** parancsmag eltávolítja az egyéni parancsfájl-kiterjesztést egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="3340e-106">The **Remove-AzureVMCustomScriptExtension** cmdlet removes the custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="3340e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3340e-107">EXAMPLES</span></span>

### <span data-ttu-id="3340e-108">Példa 1: a virtuális gép egyéni parancsfájl-bővítményének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3340e-108">Example 1: Remove a virtual machine custom script extension</span></span>
```
PS C:\> Remove-AzureVMCustomScriptExtension -VM $VM;
```

<span data-ttu-id="3340e-109">Ez a parancs eltávolítja az Azure Virtual Machine egyéni parancsfájl-bővítményét a megadott virtuális gépről a változó $VM tárolva.</span><span class="sxs-lookup"><span data-stu-id="3340e-109">This command removes the Azure virtual machine custom script extension from the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="3340e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3340e-110">PARAMETERS</span></span>

### <span data-ttu-id="3340e-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3340e-111">-InformationAction</span></span>
<span data-ttu-id="3340e-112">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="3340e-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3340e-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3340e-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3340e-114">Folytassa</span><span class="sxs-lookup"><span data-stu-id="3340e-114">Continue</span></span>
- <span data-ttu-id="3340e-115">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="3340e-115">Ignore</span></span>
- <span data-ttu-id="3340e-116">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="3340e-116">Inquire</span></span>
- <span data-ttu-id="3340e-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3340e-117">SilentlyContinue</span></span>
- <span data-ttu-id="3340e-118">állj</span><span class="sxs-lookup"><span data-stu-id="3340e-118">Stop</span></span>
- <span data-ttu-id="3340e-119">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="3340e-119">Suspend</span></span>

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

### <span data-ttu-id="3340e-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3340e-120">-InformationVariable</span></span>
<span data-ttu-id="3340e-121">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="3340e-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3340e-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="3340e-122">-Profile</span></span>
<span data-ttu-id="3340e-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="3340e-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3340e-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="3340e-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3340e-125">-VM</span><span class="sxs-lookup"><span data-stu-id="3340e-125">-VM</span></span>
<span data-ttu-id="3340e-126">Az állandó virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="3340e-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="3340e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3340e-127">CommonParameters</span></span>
<span data-ttu-id="3340e-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3340e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3340e-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3340e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3340e-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3340e-130">INPUTS</span></span>

## <span data-ttu-id="3340e-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3340e-131">OUTPUTS</span></span>

## <span data-ttu-id="3340e-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3340e-132">NOTES</span></span>

## <span data-ttu-id="3340e-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3340e-133">RELATED LINKS</span></span>

[<span data-ttu-id="3340e-134">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="3340e-134">Get-AzureVMCustomScriptExtension</span></span>](./Get-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="3340e-135">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="3340e-135">Set-AzureVMCustomScriptExtension</span></span>](./Set-AzureVMCustomScriptExtension.md)


