---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: DBB8EC31-877C-4DB1-8197-CA7A4148AE06
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f8767c9477db41251eb4732a2eb96d8dd782c20
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015531"
---
# <span data-ttu-id="11b7a-101">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="11b7a-101">Get-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="11b7a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11b7a-102">SYNOPSIS</span></span>
<span data-ttu-id="11b7a-103">Információt kap az Azure Virtual Machine egyéni parancsfájl-bővítményéről.</span><span class="sxs-lookup"><span data-stu-id="11b7a-103">Gets information from an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="11b7a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11b7a-104">SYNTAX</span></span>

```
Get-AzureVMCustomScriptExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="11b7a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="11b7a-105">DESCRIPTION</span></span>
<span data-ttu-id="11b7a-106">A **Get-AzureVMCustomScriptExtension** parancsmag az Azure Virtual Machine egyéni parancsfájl-bővítményének adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="11b7a-106">The **Get-AzureVMCustomScriptExtension** cmdlet gets information from an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="11b7a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="11b7a-107">EXAMPLES</span></span>

### <span data-ttu-id="11b7a-108">Példa 1: Azure Virtual Machine parancsfájl-bővítmény beszerzése</span><span class="sxs-lookup"><span data-stu-id="11b7a-108">Example 1: Get an Azure virtual machine script extension</span></span>
```
PS C:\> Get-AzureVMCustomScriptExtension -VM $VM;
```

<span data-ttu-id="11b7a-109">Ez a parancs a $VM változóban tárolt Azure Virtual Machine parancsfájl-kiterjesztést kap.</span><span class="sxs-lookup"><span data-stu-id="11b7a-109">This command gets an Azure virtual machine script extension stored in the variable $VM.</span></span>

## <span data-ttu-id="11b7a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11b7a-110">PARAMETERS</span></span>

### <span data-ttu-id="11b7a-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="11b7a-111">-InformationAction</span></span>
<span data-ttu-id="11b7a-112">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="11b7a-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="11b7a-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="11b7a-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="11b7a-114">Folytassa</span><span class="sxs-lookup"><span data-stu-id="11b7a-114">Continue</span></span>
- <span data-ttu-id="11b7a-115">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="11b7a-115">Ignore</span></span>
- <span data-ttu-id="11b7a-116">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="11b7a-116">Inquire</span></span>
- <span data-ttu-id="11b7a-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="11b7a-117">SilentlyContinue</span></span>
- <span data-ttu-id="11b7a-118">állj</span><span class="sxs-lookup"><span data-stu-id="11b7a-118">Stop</span></span>
- <span data-ttu-id="11b7a-119">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="11b7a-119">Suspend</span></span>

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

### <span data-ttu-id="11b7a-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="11b7a-120">-InformationVariable</span></span>
<span data-ttu-id="11b7a-121">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="11b7a-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="11b7a-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="11b7a-122">-Profile</span></span>
<span data-ttu-id="11b7a-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="11b7a-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="11b7a-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="11b7a-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="11b7a-125">-VM</span><span class="sxs-lookup"><span data-stu-id="11b7a-125">-VM</span></span>
<span data-ttu-id="11b7a-126">Az állandó virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="11b7a-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="11b7a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11b7a-127">CommonParameters</span></span>
<span data-ttu-id="11b7a-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11b7a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11b7a-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11b7a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11b7a-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11b7a-130">INPUTS</span></span>

## <span data-ttu-id="11b7a-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11b7a-131">OUTPUTS</span></span>

## <span data-ttu-id="11b7a-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11b7a-132">NOTES</span></span>

## <span data-ttu-id="11b7a-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11b7a-133">RELATED LINKS</span></span>

[<span data-ttu-id="11b7a-134">Remove-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="11b7a-134">Remove-AzureVMCustomScriptExtension</span></span>](./Remove-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="11b7a-135">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="11b7a-135">Set-AzureVMCustomScriptExtension</span></span>](./Set-AzureVMCustomScriptExtension.md)


