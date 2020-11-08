---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F5EC8E00-E504-436A-96FF-4E886579AEA4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b72fcfac0b000a8fcfc11dbab6961460cb25b8b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016415"
---
# <span data-ttu-id="05220-101">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="05220-101">Set-AzureStoreAddOn</span></span>

## <span data-ttu-id="05220-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="05220-102">SYNOPSIS</span></span>
<span data-ttu-id="05220-103">Frissít egy meglévő bővítmény-példányt.</span><span class="sxs-lookup"><span data-stu-id="05220-103">Updates an existing add-on instance.</span></span>

## <span data-ttu-id="05220-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="05220-104">SYNTAX</span></span>

```
Set-AzureStoreAddOn -Name <String> -Plan <String> [-PromotionCode <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="05220-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="05220-105">DESCRIPTION</span></span>
<span data-ttu-id="05220-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="05220-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="05220-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="05220-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="05220-108">Ez a parancsmag egy meglévő bővítményt frissít a jelenlegi előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="05220-108">This cmdlet updates an existing add-on instance from the current subscription.</span></span>

## <span data-ttu-id="05220-109">Példák</span><span class="sxs-lookup"><span data-stu-id="05220-109">EXAMPLES</span></span>

### <span data-ttu-id="05220-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="05220-110">Example 1</span></span>
```
PS C:\> Set-AzureStoreAddOn MyAddOn NewPlanId
```

<span data-ttu-id="05220-111">Ez a példa új csomag-AZONOSÍTÓval frissíti a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="05220-111">This example updates an add-on with a new plan ID.</span></span>

### <span data-ttu-id="05220-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="05220-112">Example 2</span></span>
```
PS C:\> Set-AzureStoreAddOn MyAddOn NewPlanId MyPromoCode
```

<span data-ttu-id="05220-113">Ez a példa új csomag-AZONOSÍTÓval és promóciós kóddal frissíti a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="05220-113">This example updates an add-on with a new plan ID and promotional code.</span></span>

## <span data-ttu-id="05220-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="05220-114">PARAMETERS</span></span>

### <span data-ttu-id="05220-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="05220-115">-Name</span></span>
<span data-ttu-id="05220-116">A bővítmény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="05220-116">Specifies the name of the add-on instance.</span></span>

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

### <span data-ttu-id="05220-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05220-117">-PassThru</span></span>
<span data-ttu-id="05220-118">Ha meg van adva, a parancsmag igaz értéket ad eredményül, ha a parancs sikeres és hamis, ha sikertelen.</span><span class="sxs-lookup"><span data-stu-id="05220-118">If specified, the cmdlet returns true if the command succeeds and false if it fails.</span></span>

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

### <span data-ttu-id="05220-119">-Terv</span><span class="sxs-lookup"><span data-stu-id="05220-119">-Plan</span></span>
<span data-ttu-id="05220-120">A terv AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="05220-120">Specifies the plan ID.</span></span>

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

### <span data-ttu-id="05220-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="05220-121">-Profile</span></span>
<span data-ttu-id="05220-122">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="05220-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="05220-123">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="05220-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="05220-124">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="05220-124">-PromotionCode</span></span>
<span data-ttu-id="05220-125">A promóciós kódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="05220-125">Specifies the promotional code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05220-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05220-126">CommonParameters</span></span>
<span data-ttu-id="05220-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="05220-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05220-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05220-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05220-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="05220-129">INPUTS</span></span>

## <span data-ttu-id="05220-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05220-130">OUTPUTS</span></span>

## <span data-ttu-id="05220-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="05220-131">NOTES</span></span>

## <span data-ttu-id="05220-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05220-132">RELATED LINKS</span></span>

[<span data-ttu-id="05220-133">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="05220-133">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="05220-134">Új – AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="05220-134">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="05220-135">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="05220-135">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)


