---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 793037C4-8FE5-4799-B59B-94C1605D9F4E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 593ea36e90635472db1f8568254657f782bd1200
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016201"
---
# <span data-ttu-id="86130-101">New-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="86130-101">New-AzureStoreAddOn</span></span>

## <span data-ttu-id="86130-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86130-102">SYNOPSIS</span></span>
<span data-ttu-id="86130-103">Új bővítmény-példányt vásárol.</span><span class="sxs-lookup"><span data-stu-id="86130-103">Buys a new add-on instance.</span></span>

## <span data-ttu-id="86130-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86130-104">SYNTAX</span></span>

```
New-AzureStoreAddOn -Name <String> -AddOn <String> -Plan <String> -Location <String> [-PromotionCode <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="86130-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="86130-105">DESCRIPTION</span></span>
<span data-ttu-id="86130-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="86130-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="86130-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="86130-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="86130-108">Új bővítményt vásárol az Azure áruházból.</span><span class="sxs-lookup"><span data-stu-id="86130-108">Buys a new add-on instance from the Azure Store.</span></span>

## <span data-ttu-id="86130-109">Példák</span><span class="sxs-lookup"><span data-stu-id="86130-109">EXAMPLES</span></span>

### <span data-ttu-id="86130-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="86130-110">Example 1</span></span>
```
PS C:\> New-AzureStoreAddOn -Name MyAddOn -AddOn AddonId -Plan PlanId -Location "West US"
```

<span data-ttu-id="86130-111">Ebben a példában a MyAddOn nevű bővítményt vásárolja meg egy PlanId a Nyugat-amerikai térségben.</span><span class="sxs-lookup"><span data-stu-id="86130-111">This example buys an add-on named MyAddOn with a PlanId in West US location.</span></span>

### <span data-ttu-id="86130-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="86130-112">Example 2</span></span>
```
PS C:\> New-AzureStoreAddOn -Name MyAddOn -AddOn AddonId -Plan PlanId -Location "West US" -PromotionCode MyPromoCode
```

<span data-ttu-id="86130-113">Ez a példa promóciós kódot használ a bővítmények vásárlásához.</span><span class="sxs-lookup"><span data-stu-id="86130-113">This example uses a promotional code to buy an add-on.</span></span>

## <span data-ttu-id="86130-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86130-114">PARAMETERS</span></span>

### <span data-ttu-id="86130-115">-AddOn</span><span class="sxs-lookup"><span data-stu-id="86130-115">-AddOn</span></span>
<span data-ttu-id="86130-116">A bővítmény AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="86130-116">Specifies the add-on ID.</span></span>

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

### <span data-ttu-id="86130-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="86130-117">-Location</span></span>
<span data-ttu-id="86130-118">A bővítmény példányának helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="86130-118">Specifies the add-on instance location.</span></span>

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

### <span data-ttu-id="86130-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="86130-119">-Name</span></span>
<span data-ttu-id="86130-120">A bővítmény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="86130-120">Specifies the name of the add-on instance.</span></span>

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

### <span data-ttu-id="86130-121">-Terv</span><span class="sxs-lookup"><span data-stu-id="86130-121">-Plan</span></span>
<span data-ttu-id="86130-122">A terv AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="86130-122">Specifies the plan ID.</span></span>

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

### <span data-ttu-id="86130-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="86130-123">-Profile</span></span>
<span data-ttu-id="86130-124">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="86130-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="86130-125">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="86130-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="86130-126">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="86130-126">-PromotionCode</span></span>
<span data-ttu-id="86130-127">A vásárlásra érvényes előléptetési kódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="86130-127">Specifies a promotion code to apply to the purchase.</span></span>

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

### <span data-ttu-id="86130-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86130-128">CommonParameters</span></span>
<span data-ttu-id="86130-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86130-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86130-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86130-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86130-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86130-131">INPUTS</span></span>

## <span data-ttu-id="86130-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86130-132">OUTPUTS</span></span>

## <span data-ttu-id="86130-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86130-133">NOTES</span></span>

## <span data-ttu-id="86130-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86130-134">RELATED LINKS</span></span>

[<span data-ttu-id="86130-135">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="86130-135">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="86130-136">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="86130-136">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)

[<span data-ttu-id="86130-137">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="86130-137">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


