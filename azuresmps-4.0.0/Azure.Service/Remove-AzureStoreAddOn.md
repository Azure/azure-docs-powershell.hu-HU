---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D927B159-AD68-4071-ADE3-FA2430750D72
online version: ''
schema: 2.0.0
ms.openlocfilehash: 001466cb00ad15f1cbfef6dcf9fd3ce9b931109b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016455"
---
# <span data-ttu-id="d5759-101">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="d5759-101">Remove-AzureStoreAddOn</span></span>

## <span data-ttu-id="d5759-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5759-102">SYNOPSIS</span></span>
<span data-ttu-id="d5759-103">Eltávolít egy meglévő bővítmény-példányt.</span><span class="sxs-lookup"><span data-stu-id="d5759-103">Removes an existing add-on instance.</span></span>

## <span data-ttu-id="d5759-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5759-104">SYNTAX</span></span>

```
Remove-AzureStoreAddOn -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d5759-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5759-105">DESCRIPTION</span></span>
<span data-ttu-id="d5759-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="d5759-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d5759-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d5759-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d5759-108">Eltávolít egy meglévő bővítményt az aktuális előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="d5759-108">Removes an existing add-on instance from the current subscription.</span></span>

## <span data-ttu-id="d5759-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d5759-109">EXAMPLES</span></span>

### <span data-ttu-id="d5759-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d5759-110">Example 1</span></span>
```
PS C:\> Remove-AzureStoreAddOn MyAddOn
```

<span data-ttu-id="d5759-111">Ez a példa eltávolítja a MyAddOn nevű bővítményt az aktuális előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="d5759-111">This example removes an add-on named MyAddOn from the current subscription.</span></span>

## <span data-ttu-id="d5759-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5759-112">PARAMETERS</span></span>

### <span data-ttu-id="d5759-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d5759-113">-Name</span></span>
<span data-ttu-id="d5759-114">Annak a bővítménynek a nevét adja meg, amelyből el szeretné távolítani a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="d5759-114">Specifies the name of the add-on instance to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5759-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5759-115">-PassThru</span></span>
<span data-ttu-id="d5759-116">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="d5759-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d5759-117">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="d5759-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5759-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="d5759-118">-Profile</span></span>
<span data-ttu-id="d5759-119">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d5759-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d5759-120">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d5759-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d5759-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5759-121">CommonParameters</span></span>
<span data-ttu-id="d5759-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5759-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5759-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5759-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5759-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5759-124">INPUTS</span></span>

## <span data-ttu-id="d5759-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5759-125">OUTPUTS</span></span>

## <span data-ttu-id="d5759-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5759-126">NOTES</span></span>

## <span data-ttu-id="d5759-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5759-127">RELATED LINKS</span></span>

[<span data-ttu-id="d5759-128">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="d5759-128">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="d5759-129">Új – AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="d5759-129">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="d5759-130">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="d5759-130">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


