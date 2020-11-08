---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 40AE50AA-6807-4481-8B77-A038914D462E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a4c6997a7ae70a72a21800cce1d4f5f32475a85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016447"
---
# <span data-ttu-id="62a18-101">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="62a18-101">Remove-AzureVMDscExtension</span></span>

## <span data-ttu-id="62a18-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62a18-102">SYNOPSIS</span></span>
<span data-ttu-id="62a18-103">Azure DSC-bővítmény eltávolítása virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="62a18-103">Removes an Azure DSC extension from a virtual machine.</span></span>

## <span data-ttu-id="62a18-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62a18-104">SYNTAX</span></span>

```
Remove-AzureVMDscExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62a18-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="62a18-105">DESCRIPTION</span></span>
<span data-ttu-id="62a18-106">A **Remove-AzureVMDscExtension** parancsmag eltávolítja az Azure DSC bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="62a18-106">The **Remove-AzureVMDscExtension** cmdlet removes an Azure DSC extension from a virtual machine.</span></span>
<span data-ttu-id="62a18-107">A parancsmag kimenetének az **Update-AzureVM** parancsmaghoz kell lennie.</span><span class="sxs-lookup"><span data-stu-id="62a18-107">The output of this cmdlet needs to be piped to the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="62a18-108">Példák</span><span class="sxs-lookup"><span data-stu-id="62a18-108">EXAMPLES</span></span>

### <span data-ttu-id="62a18-109">1. példa: DSC-bővítmény eltávolítása virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="62a18-109">Example 1: Remove a DSC extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMDscExtension -VM $VM | Update-AzureVM
```

<span data-ttu-id="62a18-110">Ez a parancs eltávolítja az Azure DSC bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="62a18-110">This command removes an Azure DSC extension from a virtual machine.</span></span>

## <span data-ttu-id="62a18-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62a18-111">PARAMETERS</span></span>

### <span data-ttu-id="62a18-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="62a18-112">-InformationAction</span></span>
<span data-ttu-id="62a18-113">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="62a18-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="62a18-114">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="62a18-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="62a18-115">Folytassa</span><span class="sxs-lookup"><span data-stu-id="62a18-115">Continue</span></span>
- <span data-ttu-id="62a18-116">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="62a18-116">Ignore</span></span>
- <span data-ttu-id="62a18-117">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="62a18-117">Inquire</span></span>
- <span data-ttu-id="62a18-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="62a18-118">SilentlyContinue</span></span>
- <span data-ttu-id="62a18-119">állj</span><span class="sxs-lookup"><span data-stu-id="62a18-119">Stop</span></span>
- <span data-ttu-id="62a18-120">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="62a18-120">Suspend</span></span>

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

### <span data-ttu-id="62a18-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="62a18-121">-InformationVariable</span></span>
<span data-ttu-id="62a18-122">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="62a18-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="62a18-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="62a18-123">-Profile</span></span>
<span data-ttu-id="62a18-124">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="62a18-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="62a18-125">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="62a18-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="62a18-126">-VM</span><span class="sxs-lookup"><span data-stu-id="62a18-126">-VM</span></span>
<span data-ttu-id="62a18-127">Az állandó virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="62a18-127">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="62a18-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="62a18-128">-Confirm</span></span>
<span data-ttu-id="62a18-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="62a18-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a18-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62a18-130">-WhatIf</span></span>
<span data-ttu-id="62a18-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="62a18-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62a18-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="62a18-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a18-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62a18-133">CommonParameters</span></span>
<span data-ttu-id="62a18-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62a18-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62a18-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62a18-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62a18-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62a18-136">INPUTS</span></span>

## <span data-ttu-id="62a18-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62a18-137">OUTPUTS</span></span>

## <span data-ttu-id="62a18-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62a18-138">NOTES</span></span>

## <span data-ttu-id="62a18-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62a18-139">RELATED LINKS</span></span>

[<span data-ttu-id="62a18-140">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="62a18-140">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="62a18-141">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="62a18-141">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)

[<span data-ttu-id="62a18-142">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="62a18-142">Update-AzureVM</span></span>](./Update-AzureVM.md)


