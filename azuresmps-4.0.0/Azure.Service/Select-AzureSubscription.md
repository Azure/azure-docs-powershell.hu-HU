---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 7A45DCAD-88DC-40F0-BBF7-0F531A571CA6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48b941691366c3af821e3a4cdaa7b07c5e958e16
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015445"
---
# <span data-ttu-id="c11fb-101">Select-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="c11fb-101">Select-AzureSubscription</span></span>

## <span data-ttu-id="c11fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c11fb-102">SYNOPSIS</span></span>
<span data-ttu-id="c11fb-103">Az aktuális és az alapértelmezett Azure-előfizetések módosítása</span><span class="sxs-lookup"><span data-stu-id="c11fb-103">Changes the current and default Azure subscriptions.</span></span>

## <span data-ttu-id="c11fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c11fb-104">SYNTAX</span></span>

### <span data-ttu-id="c11fb-105">SelectSubscriptionByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c11fb-105">SelectSubscriptionByNameParameterSet (Default)</span></span>
```
Select-AzureSubscription -SubscriptionName <String> [-Account <String>] [-Current] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c11fb-106">SelectDefaultSubscriptionByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c11fb-106">SelectDefaultSubscriptionByNameParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionName <String> [-Account <String>] [-Default] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c11fb-107">SelectSubscriptionByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c11fb-107">SelectSubscriptionByIdParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionId <String> [-Account <String>] [-Current] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c11fb-108">SelectDefaultSubscriptionByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c11fb-108">SelectDefaultSubscriptionByIdParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionId <String> [-Account <String>] [-Default] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c11fb-109">NoCurrentSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c11fb-109">NoCurrentSubscriptionParameterSet</span></span>
```
Select-AzureSubscription [-Account <String>] [-NoCurrent] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="c11fb-110">NoDefaultSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c11fb-110">NoDefaultSubscriptionParameterSet</span></span>
```
Select-AzureSubscription [-Account <String>] [-NoDefault] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c11fb-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="c11fb-111">DESCRIPTION</span></span>
<span data-ttu-id="c11fb-112">A **Select-AzureSubscription** parancsmag beállítja az aktuális és az alapértelmezett Azure-előfizetést, és törli őket.</span><span class="sxs-lookup"><span data-stu-id="c11fb-112">The **Select-AzureSubscription** cmdlet sets and clears the current and default Azure subscriptions.</span></span>

<span data-ttu-id="c11fb-113">Az "aktuális előfizetés" az aktuális Windows PowerShell-munkamenetben alapértelmezés szerint használt előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c11fb-113">The "current subscription" is the subscription that is used by default in the current Windows PowerShell session.</span></span>
<span data-ttu-id="c11fb-114">Az alapértelmezett előfizetés alapértelmezés szerint minden Windows PowerShell-munkamenetben használatos.</span><span class="sxs-lookup"><span data-stu-id="c11fb-114">The "default subscription" is used by default in all Windows PowerShell sessions.</span></span>
<span data-ttu-id="c11fb-115">A "jelenlegi előfizetés" címke lehetővé teszi, hogy az aktuális munkamenethez alapértelmezés szerint eltérő előfizetést adjon meg anélkül, hogy a többi munkamenethez az "alapértelmezett előfizetést" módosítaná.</span><span class="sxs-lookup"><span data-stu-id="c11fb-115">The "current subscription" label lets you specify a different subscription to be used by default for the current session without changing the "default subscription" for all other sessions.</span></span>

<span data-ttu-id="c11fb-116">Az "alapértelmezett" előfizetés-kijelölést az előfizetési adatfájl menti.</span><span class="sxs-lookup"><span data-stu-id="c11fb-116">The "default" subscription designation is saved in your subscription data file.</span></span>
<span data-ttu-id="c11fb-117">A munkamenet-specifikus "aktuális" kijelölést a program nem menti.</span><span class="sxs-lookup"><span data-stu-id="c11fb-117">The session-specific "current" designation is not saved.</span></span>

<span data-ttu-id="c11fb-118">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="c11fb-118">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c11fb-119">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c11fb-119">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="c11fb-120">Példák</span><span class="sxs-lookup"><span data-stu-id="c11fb-120">EXAMPLES</span></span>

### <span data-ttu-id="c11fb-121">Példa 1: a jelenlegi előfizetés beállítása</span><span class="sxs-lookup"><span data-stu-id="c11fb-121">Example 1: Set the current subscription</span></span>
```
C:\PS> Select-AzureSubscription -Current -SubscriptionName ContosoEngineering
```

<span data-ttu-id="c11fb-122">Ez a parancs a jelenlegi előfizetést "ContosoEngineering" teszi.</span><span class="sxs-lookup"><span data-stu-id="c11fb-122">This command makes "ContosoEngineering" the current subscription.</span></span>

### <span data-ttu-id="c11fb-123">2. példa: az alapértelmezett előfizetés beállítása</span><span class="sxs-lookup"><span data-stu-id="c11fb-123">Example 2: Set the default subscription</span></span>
```
C:\PS> Select-AzureSubscription -Default -SubscriptionName ContosoFinance -SubscriptionDataFile "C:\subs\MySubscriptions.xml"
```

<span data-ttu-id="c11fb-124">Ez a parancs megváltoztatja az alapértelmezett "ContosoFinance" előfizetést.</span><span class="sxs-lookup"><span data-stu-id="c11fb-124">This command changes the default subscription to "ContosoFinance."</span></span> <span data-ttu-id="c11fb-125">Az alapértelmezett előfizetési adatfájl helyett az Subscriptions.xml-előfizetés adatfájljába menti a beállítást.</span><span class="sxs-lookup"><span data-stu-id="c11fb-125">It saves the setting in the Subscriptions.xml subscription data file, instead of the default subscription data file.</span></span>

## <span data-ttu-id="c11fb-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c11fb-126">PARAMETERS</span></span>

### <span data-ttu-id="c11fb-127">-Fiók</span><span class="sxs-lookup"><span data-stu-id="c11fb-127">-Account</span></span>
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

### <span data-ttu-id="c11fb-128">-Current</span><span class="sxs-lookup"><span data-stu-id="c11fb-128">-Current</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: SelectSubscriptionByNameParameterSet, SelectSubscriptionByIdParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11fb-129">– Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="c11fb-129">-Default</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: SelectDefaultSubscriptionByNameParameterSet, SelectDefaultSubscriptionByIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11fb-130">-Nem aktuális</span><span class="sxs-lookup"><span data-stu-id="c11fb-130">-NoCurrent</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: NoCurrentSubscriptionParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11fb-131">– Nem alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="c11fb-131">-NoDefault</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: NoDefaultSubscriptionParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11fb-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c11fb-132">-PassThru</span></span>
<span data-ttu-id="c11fb-133">A parancs eredményét $True, ha a parancs sikerül, és a $False sikertelen.</span><span class="sxs-lookup"><span data-stu-id="c11fb-133">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="c11fb-134">Ez a parancsmag alapértelmezés szerint nem ad vissza semmilyen eredményt.</span><span class="sxs-lookup"><span data-stu-id="c11fb-134">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="c11fb-135">-Profil</span><span class="sxs-lookup"><span data-stu-id="c11fb-135">-Profile</span></span>
<span data-ttu-id="c11fb-136">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="c11fb-136">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c11fb-137">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="c11fb-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c11fb-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c11fb-138">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: SelectSubscriptionByIdParameterSet, SelectDefaultSubscriptionByIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c11fb-139">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="c11fb-139">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: SelectSubscriptionByNameParameterSet, SelectDefaultSubscriptionByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c11fb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c11fb-140">CommonParameters</span></span>
<span data-ttu-id="c11fb-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c11fb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c11fb-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c11fb-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c11fb-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c11fb-143">INPUTS</span></span>

### <span data-ttu-id="c11fb-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="c11fb-144">None</span></span>
<span data-ttu-id="c11fb-145">A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="c11fb-145">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="c11fb-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c11fb-146">OUTPUTS</span></span>

### <span data-ttu-id="c11fb-147">Nincs vagy System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c11fb-147">None or System.Boolean</span></span>
<span data-ttu-id="c11fb-148">Ha a *PassThru* paramétert használja, ez a parancsmag logikai értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="c11fb-148">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="c11fb-149">Alapértelmezés szerint az nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="c11fb-149">By default, it does not generate any output.</span></span>

## <span data-ttu-id="c11fb-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c11fb-150">NOTES</span></span>

## <span data-ttu-id="c11fb-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c11fb-151">RELATED LINKS</span></span>

[<span data-ttu-id="c11fb-152">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="c11fb-152">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="c11fb-153">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="c11fb-153">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="c11fb-154">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="c11fb-154">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


