---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 32BC6CE6-60EF-4A46-912B-8FE4FCCDF7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b91906a25d2f2d7c40f96ed07a4fd7463722023
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015537"
---
# <span data-ttu-id="9e1b5-101">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="9e1b5-101">Get-AzureSubscription</span></span>

## <span data-ttu-id="9e1b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9e1b5-102">SYNOPSIS</span></span>
<span data-ttu-id="9e1b5-103">Azure-előfizetéseket kap az Azure-fiókban.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-103">Gets  Azure subscriptions in Azure account.</span></span>

## <span data-ttu-id="9e1b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9e1b5-104">SYNTAX</span></span>

### <span data-ttu-id="9e1b5-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9e1b5-105">ByName (Default)</span></span>
```
Get-AzureSubscription [-SubscriptionName <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e1b5-106">ById</span><span class="sxs-lookup"><span data-stu-id="9e1b5-106">ById</span></span>
```
Get-AzureSubscription [-SubscriptionId <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e1b5-107">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="9e1b5-107">Default</span></span>
```
Get-AzureSubscription [-Default] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9e1b5-108">Aktuális</span><span class="sxs-lookup"><span data-stu-id="9e1b5-108">Current</span></span>
```
Get-AzureSubscription [-Current] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9e1b5-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="9e1b5-109">DESCRIPTION</span></span>
<span data-ttu-id="9e1b5-110">A **Get-AzureSubscription** parancsmag az Azure-fiókjában kapja meg az előfizetéseket.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-110">The **Get-AzureSubscription** cmdlet gets the subscriptions in your Azure account.</span></span>
<span data-ttu-id="9e1b5-111">Ezzel a parancsmaggal információkat kaphat az előfizetésről, és bekapcsolhatja az előfizetést más parancsmagokra.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-111">You can use this cmdlet to get information about the subscription and to pipe the subscription to other cmdlets.</span></span>

<span data-ttu-id="9e1b5-112">A **Get-AzureSubscription** hozzáférést kell biztosítani az Azure-fiókokhoz.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-112">**Get-AzureSubscription** requires access to your Azure accounts.</span></span>
<span data-ttu-id="9e1b5-113">A **Get-AzureSubscription** futtatása előtt futtatnia kell a **Add-AzureAccount** parancsmagot vagy azokat a parancsmagokat, amelyekkel letöltheti és telepítheti a közzétételi beállításokat tartalmazó fájlt ( **Get-AzurePublishSettingsFile** , **import-AzurePublishSettingsFile** ).</span><span class="sxs-lookup"><span data-stu-id="9e1b5-113">Before you run **Get-AzureSubscription** , you must run the **Add-AzureAccount** cmdlet or the cmdlets that download and install a publish settings file ( **Get-AzurePublishSettingsFile** , **Import-AzurePublishSettingsFile**.</span></span>

<span data-ttu-id="9e1b5-114">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-114">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9e1b5-115">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="9e1b5-115">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="9e1b5-116">Példák</span><span class="sxs-lookup"><span data-stu-id="9e1b5-116">EXAMPLES</span></span>

### <span data-ttu-id="9e1b5-117">Példa 1: az összes előfizetés lekérése</span><span class="sxs-lookup"><span data-stu-id="9e1b5-117">Example 1: Get all subscriptions</span></span>
```
C:\PS>Get-AzureSubscription
```

<span data-ttu-id="9e1b5-118">Ez a parancs beilleszti az összes előfizetést a fiókba.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-118">This command gets all subscriptions in the account.</span></span>

### <span data-ttu-id="9e1b5-119">2. példa: előfizetés kérése név alapján</span><span class="sxs-lookup"><span data-stu-id="9e1b5-119">Example 2: Get a subscription by name</span></span>
```
C:\PS>Get-AzureSubscription -SubscriptionName "MyProdSubscription"
```

<span data-ttu-id="9e1b5-120">Ez a parancs csak az "MyProdSubsciption" előfizetést kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-120">This command gets only the "MyProdSubsciption" subscription.</span></span>

### <span data-ttu-id="9e1b5-121">3. példa: az alapértelmezett előfizetés beszerzése</span><span class="sxs-lookup"><span data-stu-id="9e1b5-121">Example 3: Get the default subscription</span></span>
```
C:\PS>(Get-AzureSubscription -Default).SubscriptionName
```

<span data-ttu-id="9e1b5-122">Ez a parancs csak az alapértelmezett előfizetés nevét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-122">This command gets only the name of the default subscription.</span></span>
<span data-ttu-id="9e1b5-123">A parancs először megkapja az előfizetést, majd a dot metódus segítségével beolvassa az előfizetés **SubscriptionName** tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-123">The command first gets the subscription and then uses the dot method to get the **SubscriptionName** property of the subscription.</span></span>

### <span data-ttu-id="9e1b5-124">4. példa: a kijelölt előfizetés tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="9e1b5-124">Example 4: Get selected subscription properties</span></span>
```
C:\PS>Get-AzureSubscription -Current | Format-List -Property SubscriptionName, Certificate
```

<span data-ttu-id="9e1b5-125">Ez a parancs a jelenlegi előfizetés nevével és tanúsítvánnyal rendelkező listát ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-125">This command returns a list with the name and certificate of the current subscription.</span></span>
<span data-ttu-id="9e1b5-126">A **Get-AzureSubscription** parancsot használja a jelenlegi előfizetés beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-126">It uses a **Get-AzureSubscription** command to get the current subscription.</span></span>
<span data-ttu-id="9e1b5-127">Ezután az előfizetést a **Formátum – lista** parancsra, amely a listában kijelölt tulajdonságokat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-127">Then it pipes the subscription to a **Format-List** command that displays the selected properties in a list.</span></span>

### <span data-ttu-id="9e1b5-128">Példa 5: alternatív előfizetési adatfájl használata</span><span class="sxs-lookup"><span data-stu-id="9e1b5-128">Example 5: Use an alternate subscription data file</span></span>
```
C:\PS>Get-AzureSubscription -SubscriptionDataFile "C:\Temp\MySubscriptions.xml"
```

<span data-ttu-id="9e1b5-129">Ez a parancs előfizetéseket kap az C:\Temp\MySubscriptions.xml előfizetési adatfájlból.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-129">This command gets subscriptions from  the C:\Temp\MySubscriptions.xml subscription data file.</span></span>
<span data-ttu-id="9e1b5-130">Ha a **Add-AzureAccount** vagy az **Importálás-PublishSettingsFile** parancsmagok futtatásakor megadta a másodlagos előfizetési adatfájlt, használja a **SubscriptionDataFile** paramétert.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-130">Use the **SubscriptionDataFile** parameter if you specified an alternate subscription data file when you ran the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlets.</span></span>

## <span data-ttu-id="9e1b5-131">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9e1b5-131">PARAMETERS</span></span>

### <span data-ttu-id="9e1b5-132">-Current</span><span class="sxs-lookup"><span data-stu-id="9e1b5-132">-Current</span></span>
<span data-ttu-id="9e1b5-133">Csak a jelenlegi előfizetést kapja meg, azaz az "aktuális" néven kijelölt előfizetést.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-133">Gets only the current subscription, that is, the subscription designated as "current."</span></span> <span data-ttu-id="9e1b5-134">A **Get-AzureSubscription** alapértelmezés szerint az Azure-fiókokban található összes előfizetést kapja.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-134">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>
<span data-ttu-id="9e1b5-135">Ha egy előfizetést "current"-ként szeretne kijelölni, használja a **Select-AzureSubscription** parancsmag **aktuális** paraméterét.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-135">To designate a subscription as "current," use the **Current** parameter of the **Select-AzureSubscription** cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Current
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e1b5-136">– Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="9e1b5-136">-Default</span></span>
<span data-ttu-id="9e1b5-137">Csak az alapértelmezett előfizetést kapja meg, azaz az alapértelmezettként megjelölt előfizetést.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-137">Gets only the default subscription, that is, the subscription designated as "default."</span></span> <span data-ttu-id="9e1b5-138">A **Get-AzureSubscription** alapértelmezés szerint az Azure-fiókokban található összes előfizetést kapja.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-138">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>
<span data-ttu-id="9e1b5-139">Ha egy előfizetést "alapértelmezettként" szeretne kijelölni, használja a **Select-AzureSubscription** parancsmag **alapértelmezett** paraméterét.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-139">To designate a subscription as "default," use the **Default** parameter of the **Select-AzureSubscription** cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Default
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e1b5-140">-ExtendedDetails</span><span class="sxs-lookup"><span data-stu-id="9e1b5-140">-ExtendedDetails</span></span>
<span data-ttu-id="9e1b5-141">Az előfizetéshez tartozó kvóta-információkat ad eredményül, a szokásos beállítások mellett.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-141">Returns quota information for the subscription, in addition to the standard settings.</span></span>

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

### <span data-ttu-id="9e1b5-142">-Profil</span><span class="sxs-lookup"><span data-stu-id="9e1b5-142">-Profile</span></span>
<span data-ttu-id="9e1b5-143">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-143">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="9e1b5-144">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9e1b5-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9e1b5-145">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: ById
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e1b5-146">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="9e1b5-146">-SubscriptionName</span></span>
<span data-ttu-id="9e1b5-147">Csak a megadott előfizetést kapja.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-147">Gets only the specified subscription.</span></span>
<span data-ttu-id="9e1b5-148">Adja meg az előfizetés nevét.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-148">Enter the subscription name.</span></span>
<span data-ttu-id="9e1b5-149">Az érték megkülönbözteti a kis-és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-149">The value is case-sensitive.</span></span>
<span data-ttu-id="9e1b5-150">A helyettesítő karakterek használata nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-150">Wildcard characters are not supported.</span></span>
<span data-ttu-id="9e1b5-151">A **Get-AzureSubscription** alapértelmezés szerint az Azure-fiókokban található összes előfizetést kapja.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-151">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e1b5-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e1b5-152">CommonParameters</span></span>
<span data-ttu-id="9e1b5-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9e1b5-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e1b5-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e1b5-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e1b5-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e1b5-155">INPUTS</span></span>

### <span data-ttu-id="9e1b5-156">Nincs</span><span class="sxs-lookup"><span data-stu-id="9e1b5-156">None</span></span>
<span data-ttu-id="9e1b5-157">A **SubscriptionName** tulajdonságot név szerint, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-157">You can pipe input to the **SubscriptionName** property by name, but not by value.</span></span>

## <span data-ttu-id="9e1b5-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e1b5-158">OUTPUTS</span></span>

### <span data-ttu-id="9e1b5-159">Microsoft. WindowsAzure. commands. Utilities. Common. WindowsAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="9e1b5-159">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureSubscription</span></span>

## <span data-ttu-id="9e1b5-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9e1b5-160">NOTES</span></span>
* <span data-ttu-id="9e1b5-161">A Get-AzureSubscription a **Add-AzureAccount** és az **import-PublishSettingsFile** parancsmagok által létrehozott előfizetési adatfájlból kapja meg az adatforrást.</span><span class="sxs-lookup"><span data-stu-id="9e1b5-161">Get-AzureSubscription gets data from the subscription data file that the **Add-AzureAccount** and **Import-PublishSettingsFile** cmdlets create.</span></span>

## <span data-ttu-id="9e1b5-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e1b5-162">RELATED LINKS</span></span>

[<span data-ttu-id="9e1b5-163">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="9e1b5-163">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="9e1b5-164">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="9e1b5-164">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="9e1b5-165">Importálás – AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="9e1b5-165">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="9e1b5-166">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="9e1b5-166">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="9e1b5-167">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="9e1b5-167">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


