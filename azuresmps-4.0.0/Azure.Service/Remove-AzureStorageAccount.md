---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 679452A6-A6CA-4DC8-8E00-09E369505319
online version: ''
schema: 2.0.0
ms.openlocfilehash: 933c6de8e7baa55b2093a7ffc4ac28fede13bb5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016458"
---
# <span data-ttu-id="1cf33-101">Remove-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1cf33-101">Remove-AzureStorageAccount</span></span>

## <span data-ttu-id="1cf33-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1cf33-102">SYNOPSIS</span></span>
<span data-ttu-id="1cf33-103">Törli a megadott tárterület-fiókot egy előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="1cf33-103">Deletes the specified storage account from a subscription.</span></span>

## <span data-ttu-id="1cf33-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1cf33-104">SYNTAX</span></span>

```
Remove-AzureStorageAccount [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1cf33-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1cf33-105">DESCRIPTION</span></span>
<span data-ttu-id="1cf33-106">A **Remove-AzureStorageAccount** parancsmag az Azure-előfizetésből eltávolítja a fiókot.</span><span class="sxs-lookup"><span data-stu-id="1cf33-106">The **Remove-AzureStorageAccount** cmdlet removes an account from an Azure subscription.</span></span>

## <span data-ttu-id="1cf33-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1cf33-107">EXAMPLES</span></span>

### <span data-ttu-id="1cf33-108">1. példa: tárterület-fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1cf33-108">Example 1: Remove a storage account</span></span>
```
PS C:\> Remove-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="1cf33-109">Ez a parancs eltávolítja a ContosoStore01-tároló fiókot a megadott előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="1cf33-109">This command removes the ContosoStore01 storage account from the specified subscription.</span></span>

## <span data-ttu-id="1cf33-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1cf33-110">PARAMETERS</span></span>

### <span data-ttu-id="1cf33-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1cf33-111">-InformationAction</span></span>
<span data-ttu-id="1cf33-112">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="1cf33-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1cf33-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="1cf33-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1cf33-114">Folytassa</span><span class="sxs-lookup"><span data-stu-id="1cf33-114">Continue</span></span>
- <span data-ttu-id="1cf33-115">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="1cf33-115">Ignore</span></span>
- <span data-ttu-id="1cf33-116">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="1cf33-116">Inquire</span></span>
- <span data-ttu-id="1cf33-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1cf33-117">SilentlyContinue</span></span>
- <span data-ttu-id="1cf33-118">állj</span><span class="sxs-lookup"><span data-stu-id="1cf33-118">Stop</span></span>
- <span data-ttu-id="1cf33-119">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="1cf33-119">Suspend</span></span>

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

### <span data-ttu-id="1cf33-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1cf33-120">-InformationVariable</span></span>
<span data-ttu-id="1cf33-121">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="1cf33-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1cf33-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="1cf33-122">-Profile</span></span>
<span data-ttu-id="1cf33-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="1cf33-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1cf33-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="1cf33-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1cf33-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1cf33-125">-StorageAccountName</span></span>
<span data-ttu-id="1cf33-126">Az eltávolítandó tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1cf33-126">Specifies the name of the storage account to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cf33-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cf33-127">CommonParameters</span></span>
<span data-ttu-id="1cf33-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1cf33-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cf33-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cf33-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cf33-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1cf33-130">INPUTS</span></span>

## <span data-ttu-id="1cf33-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1cf33-131">OUTPUTS</span></span>

## <span data-ttu-id="1cf33-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1cf33-132">NOTES</span></span>

## <span data-ttu-id="1cf33-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1cf33-133">RELATED LINKS</span></span>

[<span data-ttu-id="1cf33-134">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1cf33-134">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="1cf33-135">Új – AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1cf33-135">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="1cf33-136">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1cf33-136">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


