---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A513B7CA-182E-46A2-8181-020C5DFC7DE9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 316e7c182025171d2f1ba66ead1a0c0f5de120b1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015504"
---
# <span data-ttu-id="fb09f-101">Remove-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="fb09f-101">Remove-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="fb09f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb09f-102">SYNOPSIS</span></span>
<span data-ttu-id="fb09f-103">Eltávolítja az Azure Diagnostics bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="fb09f-103">Removes the Azure Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="fb09f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb09f-104">SYNTAX</span></span>

```
Remove-AzureVMDiagnosticsExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fb09f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb09f-105">DESCRIPTION</span></span>
<span data-ttu-id="fb09f-106">A **Remove-AzureVMDiagnosticsExtension** parancsmag eltávolítja a Microsoft Azure Diagnostics bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="fb09f-106">The **Remove-AzureVMDiagnosticsExtension** cmdlet removes a Microsoft Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="fb09f-107">Át kell adnia a parancsmag kimenetét a **Update-AzureVM** parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="fb09f-107">You must pass the output of this cmdlet to the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="fb09f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="fb09f-108">EXAMPLES</span></span>

### <span data-ttu-id="fb09f-109">1. példa: az Azure Diagnostics bővítmény eltávolítása virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="fb09f-109">Example 1: Remove the Azure Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMDiagnosticsExtension -VM $VM | Update-AzureVM
```

<span data-ttu-id="fb09f-110">Ez a parancs eltávolítja az Azure Diagnostics bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="fb09f-110">This command removes the Azure Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="fb09f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb09f-111">PARAMETERS</span></span>

### <span data-ttu-id="fb09f-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="fb09f-112">-InformationAction</span></span>
<span data-ttu-id="fb09f-113">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="fb09f-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fb09f-114">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="fb09f-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fb09f-115">Folytassa</span><span class="sxs-lookup"><span data-stu-id="fb09f-115">Continue</span></span>
- <span data-ttu-id="fb09f-116">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="fb09f-116">Ignore</span></span>
- <span data-ttu-id="fb09f-117">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="fb09f-117">Inquire</span></span>
- <span data-ttu-id="fb09f-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fb09f-118">SilentlyContinue</span></span>
- <span data-ttu-id="fb09f-119">állj</span><span class="sxs-lookup"><span data-stu-id="fb09f-119">Stop</span></span>
- <span data-ttu-id="fb09f-120">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="fb09f-120">Suspend</span></span>

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

### <span data-ttu-id="fb09f-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fb09f-121">-InformationVariable</span></span>
<span data-ttu-id="fb09f-122">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="fb09f-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fb09f-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="fb09f-123">-Profile</span></span>
<span data-ttu-id="fb09f-124">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="fb09f-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fb09f-125">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="fb09f-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fb09f-126">-VM</span><span class="sxs-lookup"><span data-stu-id="fb09f-126">-VM</span></span>
<span data-ttu-id="fb09f-127">Az állandó virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb09f-127">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="fb09f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb09f-128">CommonParameters</span></span>
<span data-ttu-id="fb09f-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb09f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb09f-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb09f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb09f-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb09f-131">INPUTS</span></span>

## <span data-ttu-id="fb09f-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb09f-132">OUTPUTS</span></span>

## <span data-ttu-id="fb09f-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb09f-133">NOTES</span></span>

## <span data-ttu-id="fb09f-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb09f-134">RELATED LINKS</span></span>

[<span data-ttu-id="fb09f-135">Get-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="fb09f-135">Get-AzureVMDiagnosticsExtension</span></span>](./Get-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="fb09f-136">Set-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="fb09f-136">Set-AzureVMDiagnosticsExtension</span></span>](./Set-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="fb09f-137">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="fb09f-137">Update-AzureVM</span></span>](./Update-AzureVM.md)


