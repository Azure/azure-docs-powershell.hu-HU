---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E4B1AA31-1185-4035-86E6-2BB2587285C6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8273613081ab6bab0c9c3481df90f5b680b3355
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016274"
---
# <span data-ttu-id="d10cc-101">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d10cc-101">Get-AzureWebsite</span></span>

## <span data-ttu-id="d10cc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d10cc-102">SYNOPSIS</span></span>
<span data-ttu-id="d10cc-103">Azure-webhelyeket kap az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="d10cc-103">Gets Azure websites in the current subscription.</span></span>

## <span data-ttu-id="d10cc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d10cc-104">SYNTAX</span></span>

```
Get-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d10cc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d10cc-105">DESCRIPTION</span></span>
<span data-ttu-id="d10cc-106">A **Get-AzureWebsite** parancsmag a jelenlegi előfizetésben az Azure-webhelyekkel kapcsolatos információkat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d10cc-106">The **Get-AzureWebsite** cmdlet gets information about Azure websites in the current subscription.</span></span>

<span data-ttu-id="d10cc-107">Alapértelmezés szerint a **Get-AzureWebsite** megkapja az összes Azure-webhelyet a jelenlegi előfizetésben, és egy olyan objektumot ad eredményül, amely alapvető információkat nyújt a webhelyekről.</span><span class="sxs-lookup"><span data-stu-id="d10cc-107">By default, **Get-AzureWebsite** gets all Azure websites in the current subscription and returns an object that provides basic information about the sites.</span></span>
<span data-ttu-id="d10cc-108">A *Name* paraméter használatakor a **Get-AzureWebsite** olyan objektumot ad eredményül, amely részletes információkat tartalmaz, például a konfigurációs adatokat.</span><span class="sxs-lookup"><span data-stu-id="d10cc-108">When you use the *Name* parameter, **Get-AzureWebsite** returns an object with extensive information, including configuration details.</span></span>

<span data-ttu-id="d10cc-109">A jelenlegi előfizetés a "current" (aktuális) jelölt előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d10cc-109">The current subscription is the subscription that is designated as "current."</span></span> <span data-ttu-id="d10cc-110">Az aktuális előfizetés megkereséséhez használja a [Get-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) parancsmag *aktuális* paraméterét.</span><span class="sxs-lookup"><span data-stu-id="d10cc-110">To find the current subscription, use the *Current* parameter of the [Get-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) cmdlet.</span></span>
<span data-ttu-id="d10cc-111">Az aktuális előfizetés módosításához használja a [Select-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d10cc-111">To change the current subscription, use the [Select-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) cmdlet.</span></span>

<span data-ttu-id="d10cc-112">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="d10cc-112">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d10cc-113">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d10cc-113">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="d10cc-114">Példák</span><span class="sxs-lookup"><span data-stu-id="d10cc-114">EXAMPLES</span></span>

### <span data-ttu-id="d10cc-115">Példa 1: az előfizetés összes webhelyének beszerzése</span><span class="sxs-lookup"><span data-stu-id="d10cc-115">Example 1: Get all websites in the subscription</span></span>
```
PS C:\> Get-AzureWebsite
```

<span data-ttu-id="d10cc-116">Ez a parancs a jelenlegi előfizetés összes Azure-webhelyét bekapja.</span><span class="sxs-lookup"><span data-stu-id="d10cc-116">This command gets all Azure websites in the current subscription.</span></span>

### <span data-ttu-id="d10cc-117">2. példa: webhely beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="d10cc-117">Example 2: Get a website by name</span></span>
```
PS C:\> Get-AzureWebsite -Name ContosoWeb
```

<span data-ttu-id="d10cc-118">Ez a parancs részletes információkat kap a ContosoWeb Azure webhelyről, például a konfigurációs adatokról.</span><span class="sxs-lookup"><span data-stu-id="d10cc-118">This command gets detailed information about the ContosoWeb Azure website, including configuration information.</span></span>
<span data-ttu-id="d10cc-119">A *Name* paraméter használatakor a **Get-AzureWebsite** olyan **SiteWithConfig** -objektumot ad eredményül, amely a webhellyel kapcsolatos kiterjesztett információkat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="d10cc-119">When you use the *Name* parameter, **Get-AzureWebsite** returns a **SiteWithConfig** object with extended information about the website.</span></span>

### <span data-ttu-id="d10cc-120">3. példa: részletes információk kérése az összes webhelyről</span><span class="sxs-lookup"><span data-stu-id="d10cc-120">Example 3: Get detailed information about all websites</span></span>
```
PS C:\> Get-AzureWebsite | ForEach-Object {Get-AzureWebsite -Name $_.Name}
```

<span data-ttu-id="d10cc-121">Ez a parancs részletes információkat kap az előfizetésben szereplő összes webhelyről.</span><span class="sxs-lookup"><span data-stu-id="d10cc-121">This command gets detailed information about all websites in the subscription.</span></span>
<span data-ttu-id="d10cc-122">A **Get-AzureWebsite** parancsot használja az összes webhely letöltéséhez, majd a **foreach-Object** parancsmagot használja az egyes webhelyek név szerinti beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="d10cc-122">It uses a **Get-AzureWebsite** command to get all websites and then uses the **ForEach-Object** cmdlet to get each website by name.</span></span>

### <span data-ttu-id="d10cc-123">4. példa: információk beszerzése a telepítő bővítőhelyről</span><span class="sxs-lookup"><span data-stu-id="d10cc-123">Example 4: Get information about a deployment slot</span></span>
```
PS C:\> Get-AzureWebsite -Name ContosoWeb -Slot Staging
```

<span data-ttu-id="d10cc-124">Ez a parancs beolvassa a ContosoWeb webhely átmeneti telepítési tárolóhelyét.</span><span class="sxs-lookup"><span data-stu-id="d10cc-124">This command gets the Staging deployment slot of the ContosoWeb website.</span></span>
<span data-ttu-id="d10cc-125">A központi telepítő bővítőhelyek segítségével tesztelheti az Azure-webhely különböző verzióit, és nem szabadíthatja fel őket a nyilvánosság számára.</span><span class="sxs-lookup"><span data-stu-id="d10cc-125">Deployment slots let you test different versions of your Azure website without releasing them to the public.</span></span>

### <span data-ttu-id="d10cc-126">Példa 5: webhelyek példányainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="d10cc-126">Example 5: Get website instances</span></span>
```
PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances

InstanceId
----------
2d8e712fb8f85d061c30fd793a534e6700a175f9a9ab12ca55cb3b0edfcc10ee
5834916b8cef49249b18187708223a33fbbc4352d33b48369f3166644bdd3445

PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances.Count
2
```

<span data-ttu-id="d10cc-127">Az ebben a példában szereplő parancsok az Azure-webhelyek példányok tulajdonságát használják a jelenleg futó webhely-példányokkal kapcsolatos információk megjelenítéséhez.</span><span class="sxs-lookup"><span data-stu-id="d10cc-127">The commands in this example use the Instances property of an Azure website to get information about currently running website instances.</span></span>
<span data-ttu-id="d10cc-128">A **instances** tulajdonság az Azure-modul 0.8.3 a **SiteWithConfig** objektumba lett hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="d10cc-128">The **Instances** property was added to the **SiteWithConfig** object in version 0.8.3 of the Azure module.</span></span>

<span data-ttu-id="d10cc-129">Az első parancs a webhely összes aktuális példányának példány-azonosítóját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d10cc-129">The first command gets the instance IDs of all currently running instances of a website.</span></span>
<span data-ttu-id="d10cc-130">A második parancs a webhely futó példányainak számát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d10cc-130">The second command gets the number of running instances of the website.</span></span>
<span data-ttu-id="d10cc-131">Használhatja a **Count** tulajdonságot bármely tömbben.</span><span class="sxs-lookup"><span data-stu-id="d10cc-131">You can use the **Count** property on any array.</span></span>

## <span data-ttu-id="d10cc-132">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d10cc-132">PARAMETERS</span></span>

### <span data-ttu-id="d10cc-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d10cc-133">-Name</span></span>
<span data-ttu-id="d10cc-134">Részletes konfigurációs információkat kap a megadott webhelyről.</span><span class="sxs-lookup"><span data-stu-id="d10cc-134">Gets detailed configuration information about the specified website.</span></span>
<span data-ttu-id="d10cc-135">Adja meg az előfizetés egyik webhelyének a nevét.</span><span class="sxs-lookup"><span data-stu-id="d10cc-135">Enter the name of one website in the subscription.</span></span>
<span data-ttu-id="d10cc-136">A **Get-AzureWebsite** alapértelmezés szerint a jelenlegi előfizetés összes webhelyét kapja.</span><span class="sxs-lookup"><span data-stu-id="d10cc-136">By default, **Get-AzureWebsite** gets all websites in the current subscription.</span></span>
<span data-ttu-id="d10cc-137">A *név* érték nem támogatja a helyettesítő karaktereket.</span><span class="sxs-lookup"><span data-stu-id="d10cc-137">The *Name* value does not support wildcard characters.</span></span>

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

### <span data-ttu-id="d10cc-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="d10cc-138">-Profile</span></span>
<span data-ttu-id="d10cc-139">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d10cc-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d10cc-140">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d10cc-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d10cc-141">-Slot</span><span class="sxs-lookup"><span data-stu-id="d10cc-141">-Slot</span></span>
<span data-ttu-id="d10cc-142">A webhely megadott központi telepítő tárolóhelyének beolvasása</span><span class="sxs-lookup"><span data-stu-id="d10cc-142">Gets the specified deployment slot of the website.</span></span>
<span data-ttu-id="d10cc-143">Adja meg a bővítőhely nevét (például "staging" vagy "termelés").</span><span class="sxs-lookup"><span data-stu-id="d10cc-143">Enter the slot name, such as "Staging" or "Production".</span></span>
<span data-ttu-id="d10cc-144">A telepítő bővítőhelyekről a Microsoft Azure webhelyek szakaszos központi telepítésének bemutatása című témakörben olvashat bővebben https://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/ .</span><span class="sxs-lookup"><span data-stu-id="d10cc-144">For more information about deployment slots, see Staged Deployment on Microsoft Azure Web Siteshttps://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/.</span></span>
<span data-ttu-id="d10cc-145">Ha egy meglévő Azure-webhelyhez szeretne telepítő bővítőhelyet hozzáadni, használja az Set-AzureWebsite parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d10cc-145">To add a deployment slot to an existing Azure website, use the Set-AzureWebsite cmdlet.</span></span>

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

### <span data-ttu-id="d10cc-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d10cc-146">CommonParameters</span></span>
<span data-ttu-id="d10cc-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d10cc-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d10cc-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d10cc-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d10cc-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d10cc-149">INPUTS</span></span>

### <span data-ttu-id="d10cc-150">Nincs</span><span class="sxs-lookup"><span data-stu-id="d10cc-150">None</span></span>
<span data-ttu-id="d10cc-151">A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="d10cc-151">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="d10cc-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d10cc-152">OUTPUTS</span></span>

### <span data-ttu-id="d10cc-153">Microsoft. WindowsAzure. Command. Utilities. websites. Services. webentitások. webhely</span><span class="sxs-lookup"><span data-stu-id="d10cc-153">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.Site</span></span>
<span data-ttu-id="d10cc-154">Alapértelmezés szerint a **Get-AzureWebsite** a **webhely** objektumainak tömbjét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="d10cc-154">By default, **Get-AzureWebsite** returns an array of **Site** objects.</span></span>

### <span data-ttu-id="d10cc-155">Microsoft. WindowsAzure. Command. Utilities. websites. Services. webentitások. SiteWithConfig</span><span class="sxs-lookup"><span data-stu-id="d10cc-155">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.SiteWithConfig</span></span>
<span data-ttu-id="d10cc-156">A *Name* paraméter használatakor a **Get-AzureWebsite** egy **SiteWithConfig** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="d10cc-156">When you use the *Name* parameter, **Get-AzureWebsite** returns a **SiteWithConfig** object.</span></span>

## <span data-ttu-id="d10cc-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d10cc-157">NOTES</span></span>

## <span data-ttu-id="d10cc-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d10cc-158">RELATED LINKS</span></span>

[<span data-ttu-id="d10cc-159">Új – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d10cc-159">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="d10cc-160">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d10cc-160">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="d10cc-161">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d10cc-161">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="d10cc-162">Stop-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d10cc-162">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)

[<span data-ttu-id="d10cc-163">Show-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d10cc-163">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)


