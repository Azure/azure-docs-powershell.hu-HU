---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: ABC303ED-8712-4958-B871-E95357012277
online version: ''
schema: 2.0.0
ms.openlocfilehash: 706c1dee2bc4bb21a8cf116d15bfa3e53daeed99
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016095"
---
# <span data-ttu-id="dca1a-101">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="dca1a-101">Remove-AzureSubscription</span></span>

## <span data-ttu-id="dca1a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dca1a-102">SYNOPSIS</span></span>
<span data-ttu-id="dca1a-103">Azure-előfizetés törlése a Windows PowerShellből</span><span class="sxs-lookup"><span data-stu-id="dca1a-103">Deletes an Azure subscription from Windows PowerShell.</span></span>

## <span data-ttu-id="dca1a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dca1a-104">SYNTAX</span></span>

### <span data-ttu-id="dca1a-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dca1a-105">Name (Default)</span></span>
```
Remove-AzureSubscription -SubscriptionName <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dca1a-106">Azonosító</span><span class="sxs-lookup"><span data-stu-id="dca1a-106">Id</span></span>
```
Remove-AzureSubscription -SubscriptionId <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dca1a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dca1a-107">DESCRIPTION</span></span>
<span data-ttu-id="dca1a-108">A **Remove-AzureSubscription** parancsmag Azure-előfizetést töröl az előfizetési adatfájlból, így a Windows PowerShell nem találja.</span><span class="sxs-lookup"><span data-stu-id="dca1a-108">The **Remove-AzureSubscription** cmdlet deletes an Azure subscription from your subscription data file so Windows PowerShell can't find it.</span></span>
<span data-ttu-id="dca1a-109">Ez a parancsmag nem törli a Microsoft Azure-előfizetést, vagy semmilyen módon nem változtatja meg a tényleges előfizetést.</span><span class="sxs-lookup"><span data-stu-id="dca1a-109">This cmdlet does not delete the subscription from Microsoft Azure, or change the actual subscription in any way.</span></span>

<span data-ttu-id="dca1a-110">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="dca1a-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="dca1a-111">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="dca1a-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="dca1a-112">Példák</span><span class="sxs-lookup"><span data-stu-id="dca1a-112">EXAMPLES</span></span>

### <span data-ttu-id="dca1a-113">Példa 1: előfizetés törlése</span><span class="sxs-lookup"><span data-stu-id="dca1a-113">Example 1: Delete a subscription</span></span>
```
C:\PS> Remove-AzureSubscription -SubscriptionName Test

Confirm
Are you sure you want to perform this action?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="dca1a-114">Ez a parancs törli a "teszt" előfizetést az alapértelmezett előfizetési adatfájlból.</span><span class="sxs-lookup"><span data-stu-id="dca1a-114">This command deletes the "Test" subscription from the default subscription data file.</span></span>

### <span data-ttu-id="dca1a-115">2. példa: törlés másik előfizetési adatfájlból</span><span class="sxs-lookup"><span data-stu-id="dca1a-115">Example 2: Delete from an alternate subscription data file</span></span>
```
C:\PS> Remove-AzureSubscription -SubscriptionName Test -SubscriptionDataFile C:\Subs\MySubscriptions.xml -Force
```

<span data-ttu-id="dca1a-116">Ez a parancs törli a teszt-előfizetést az MySubscriptions.xml-előfizetési adatfájlból.</span><span class="sxs-lookup"><span data-stu-id="dca1a-116">This command deletes the Test subscription from the MySubscriptions.xml subscription data file.</span></span>
<span data-ttu-id="dca1a-117">A parancs az *erő* paramétert használja a megerősítési kérdés elrejtéséhez.</span><span class="sxs-lookup"><span data-stu-id="dca1a-117">The command uses the *Force* parameter to suppress the confirmation prompt.</span></span>

### <span data-ttu-id="dca1a-118">3. példa: előfizetés törlése parancsfájlból</span><span class="sxs-lookup"><span data-stu-id="dca1a-118">Example 3: Delete a subscription in a script</span></span>
```
C:\PS> ...if (Remove-AzureSubscription -SubscriptionName Test -PassThru) {...}
```

<span data-ttu-id="dca1a-119">Ez a parancs a **Ha** utasításban a **Remove-AzureSubscription** parancsot használja.</span><span class="sxs-lookup"><span data-stu-id="dca1a-119">This command uses the **Remove-AzureSubscription** command in an **If** statement.</span></span>
<span data-ttu-id="dca1a-120">A *PassThru* paramétert használja, amely logikai értéket ad eredményül annak megállapításához, hogy a parancsfájl blokkolva van-e a **Ha** utasításban.</span><span class="sxs-lookup"><span data-stu-id="dca1a-120">It uses the *PassThru* parameter, which returns a Boolean value, to determine whether the script block in the **If** statement is executed.</span></span>

## <span data-ttu-id="dca1a-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dca1a-121">PARAMETERS</span></span>

### <span data-ttu-id="dca1a-122">-Force</span><span class="sxs-lookup"><span data-stu-id="dca1a-122">-Force</span></span>
<span data-ttu-id="dca1a-123">Letiltja a megerősítési kérdést.</span><span class="sxs-lookup"><span data-stu-id="dca1a-123">Suppresses the confirmation prompt.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca1a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dca1a-124">-PassThru</span></span>
<span data-ttu-id="dca1a-125">A parancs eredményét $True, ha a parancs sikerül, és a $False sikertelen.</span><span class="sxs-lookup"><span data-stu-id="dca1a-125">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="dca1a-126">Ez a parancsmag alapértelmezés szerint nem ad vissza semmilyen eredményt.</span><span class="sxs-lookup"><span data-stu-id="dca1a-126">By default, this cmdlet does not return any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca1a-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="dca1a-127">-Profile</span></span>
<span data-ttu-id="dca1a-128">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="dca1a-128">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="dca1a-129">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="dca1a-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dca1a-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dca1a-130">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: Id
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dca1a-131">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="dca1a-131">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: Name
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dca1a-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dca1a-132">-Confirm</span></span>
<span data-ttu-id="dca1a-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dca1a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dca1a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dca1a-134">-WhatIf</span></span>
<span data-ttu-id="dca1a-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dca1a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dca1a-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dca1a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dca1a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dca1a-137">CommonParameters</span></span>
<span data-ttu-id="dca1a-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dca1a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dca1a-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dca1a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dca1a-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dca1a-140">INPUTS</span></span>

### <span data-ttu-id="dca1a-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="dca1a-141">None</span></span>
<span data-ttu-id="dca1a-142">A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="dca1a-142">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="dca1a-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dca1a-143">OUTPUTS</span></span>

### <span data-ttu-id="dca1a-144">Nincs vagy System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dca1a-144">None or System.Boolean</span></span>
<span data-ttu-id="dca1a-145">Ha a *PassThru* paramétert használja, ez a parancsmag logikai értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="dca1a-145">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="dca1a-146">Ellenkező esetben nem ad vissza semmilyen eredményt.</span><span class="sxs-lookup"><span data-stu-id="dca1a-146">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="dca1a-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dca1a-147">NOTES</span></span>

## <span data-ttu-id="dca1a-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dca1a-148">RELATED LINKS</span></span>

[<span data-ttu-id="dca1a-149">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="dca1a-149">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="dca1a-150">Select-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="dca1a-150">Select-AzureSubscription</span></span>](./Select-AzureSubscription.md)

[<span data-ttu-id="dca1a-151">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="dca1a-151">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


