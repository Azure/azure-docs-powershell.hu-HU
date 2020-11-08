---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C19A1DC0-47FA-4687-B81F-315EA04AD4A8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22591c1aa5a670e8f0d73f206ed6d2bcbe52c88f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015494"
---
# <span data-ttu-id="6f0c0-101">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="6f0c0-101">Remove-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="6f0c0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6f0c0-102">SYNOPSIS</span></span>
<span data-ttu-id="6f0c0-103">Azure Virtual Machine SQL Server-bővítmény eltávolítása egy virtuálisgép-objektumból.</span><span class="sxs-lookup"><span data-stu-id="6f0c0-103">Removes an Azure virtual machine SQL Server extension from a virtual machine object.</span></span>

## <span data-ttu-id="6f0c0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6f0c0-104">SYNTAX</span></span>

```
Remove-AzureVMSqlServerExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6f0c0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6f0c0-105">DESCRIPTION</span></span>
<span data-ttu-id="6f0c0-106">A **Remove-AzureVMSqlServerExtension** parancsmag egy virtuális Machine-objektumból távolítja el az Azure Virtual Machine SQL Server bővítményét.</span><span class="sxs-lookup"><span data-stu-id="6f0c0-106">The **Remove-AzureVMSqlServerExtension** cmdlet removes an Azure virtual machine SQL Server extension from a virtual machine object.</span></span>

## <span data-ttu-id="6f0c0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6f0c0-107">EXAMPLES</span></span>

### <span data-ttu-id="6f0c0-108">1:</span><span class="sxs-lookup"><span data-stu-id="6f0c0-108">1:</span></span>
```

```

## <span data-ttu-id="6f0c0-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6f0c0-109">PARAMETERS</span></span>

### <span data-ttu-id="6f0c0-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6f0c0-110">-InformationAction</span></span>
<span data-ttu-id="6f0c0-111">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="6f0c0-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6f0c0-112">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="6f0c0-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6f0c0-113">Folytassa</span><span class="sxs-lookup"><span data-stu-id="6f0c0-113">Continue</span></span>
- <span data-ttu-id="6f0c0-114">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="6f0c0-114">Ignore</span></span>
- <span data-ttu-id="6f0c0-115">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="6f0c0-115">Inquire</span></span>
- <span data-ttu-id="6f0c0-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6f0c0-116">SilentlyContinue</span></span>
- <span data-ttu-id="6f0c0-117">állj</span><span class="sxs-lookup"><span data-stu-id="6f0c0-117">Stop</span></span>
- <span data-ttu-id="6f0c0-118">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="6f0c0-118">Suspend</span></span>

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

### <span data-ttu-id="6f0c0-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6f0c0-119">-InformationVariable</span></span>
<span data-ttu-id="6f0c0-120">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="6f0c0-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6f0c0-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="6f0c0-121">-Profile</span></span>
<span data-ttu-id="6f0c0-122">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="6f0c0-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6f0c0-123">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="6f0c0-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6f0c0-124">-VM</span><span class="sxs-lookup"><span data-stu-id="6f0c0-124">-VM</span></span>
<span data-ttu-id="6f0c0-125">Azt a állandó virtuálisgép-objektumot adja meg, amelyre a parancsmag eltávolítja a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="6f0c0-125">Specifies the persistent virtual machine object that this cmdlet removes the extension from.</span></span>

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

### <span data-ttu-id="6f0c0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f0c0-126">CommonParameters</span></span>
<span data-ttu-id="6f0c0-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6f0c0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f0c0-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f0c0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f0c0-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f0c0-129">INPUTS</span></span>

## <span data-ttu-id="6f0c0-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f0c0-130">OUTPUTS</span></span>

## <span data-ttu-id="6f0c0-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6f0c0-131">NOTES</span></span>

## <span data-ttu-id="6f0c0-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f0c0-132">RELATED LINKS</span></span>

[<span data-ttu-id="6f0c0-133">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="6f0c0-133">Get-AzureVMSqlServerExtension</span></span>](./Get-AzureVMSqlServerExtension.md)

[<span data-ttu-id="6f0c0-134">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="6f0c0-134">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


