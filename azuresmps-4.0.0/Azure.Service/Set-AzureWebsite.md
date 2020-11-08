---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9D821623-DEF9-49E4-9C44-10643A92A2E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7f6690aa45125a0d1b3383b08443234f47a1f7e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015433"
---
# <span data-ttu-id="a8afb-101">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a8afb-101">Set-AzureWebsite</span></span>

## <span data-ttu-id="a8afb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8afb-102">SYNOPSIS</span></span>
<span data-ttu-id="a8afb-103">Az Azure-ban futó webhelyek beállítása.</span><span class="sxs-lookup"><span data-stu-id="a8afb-103">Configures a website running in Azure.</span></span>

## <span data-ttu-id="a8afb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8afb-104">SYNTAX</span></span>

```
Set-AzureWebsite [-NumberOfWorkers <Int32>] [-DefaultDocuments <String[]>] [-NetFrameworkVersion <String>]
 [-PhpVersion <String>] [-RequestTracingEnabled <Boolean>] [-HttpLoggingEnabled <Boolean>]
 [-DetailedErrorLoggingEnabled <Boolean>] [-HostNames <String[]>] [-AppSettings <Hashtable>]
 [-Metadata <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.NameValuePair]>]
 [-ConnectionStrings <ConnStringPropertyBag>] [-HandlerMappings <HandlerMapping[]>]
 [-SiteWithConfig <SiteWithConfig>] [-PassThru] [-ManagedPipelineMode <ManagedPipelineMode>]
 [-WebSocketsEnabled <Boolean>]
 [-RoutingRules <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.RoutingRule]>]
 [-Use32BitWorkerProcess <Boolean>] [-AutoSwapSlotName <String>]
 [-SlotStickyAppSettingNames <System.Collections.Generic.List`1[System.String]>]
 [-SlotStickyConnectionStringNames <System.Collections.Generic.List`1[System.String]>] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a8afb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8afb-105">DESCRIPTION</span></span>
<span data-ttu-id="a8afb-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="a8afb-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a8afb-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a8afb-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a8afb-108">A **set-AzureWebsite** parancsmag az Azure-ban futó webhelyet állítja be.</span><span class="sxs-lookup"><span data-stu-id="a8afb-108">The **Set-AzureWebsite** cmdlet configures a website running in Azure.</span></span>

## <span data-ttu-id="a8afb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a8afb-109">EXAMPLES</span></span>

### <span data-ttu-id="a8afb-110">Példa 1: a HTTP-naplózás engedélyezése egy webhelyhez</span><span class="sxs-lookup"><span data-stu-id="a8afb-110">Example 1: Enable HTTP logging for a website</span></span>
```
PS C:\> Set-AzureWebsite -HttpLoggingEnabled 1
```

<span data-ttu-id="a8afb-111">Ez a példa engedélyezi a HTTP-naplózást.</span><span class="sxs-lookup"><span data-stu-id="a8afb-111">This example enables HTTP logging.</span></span>

### <span data-ttu-id="a8afb-112">2. példa: tárterület-hitelesítő adatok beállítása webhelyhez</span><span class="sxs-lookup"><span data-stu-id="a8afb-112">Example 2: Set storage credentials for a website</span></span>
```
PS C:\> $settings = New-Object Hashtable$settings["AZURE_STORAGE_ACCOUNT"= myaccountname$settings["AZURE_STORAGE_ACCESS_KEY"] = myaccesskeySet-AzureWebsite -AppSettings $settings myWebsite
```

<span data-ttu-id="a8afb-113">Ez a példa a myWebsite nevű webhelyre állítja be a tárolási hitelesítő adatokat AZURE_STORAGE_ACCOUNT és AZURE_STORAGE_ACCESS_KEY környezeti változói szerint.</span><span class="sxs-lookup"><span data-stu-id="a8afb-113">This example sets storage credentials in a website named myWebsite with environment variables for AZURE_STORAGE_ACCOUNT and AZURE_STORAGE_ACCESS_KEY.</span></span>

## <span data-ttu-id="a8afb-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8afb-114">PARAMETERS</span></span>

### <span data-ttu-id="a8afb-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="a8afb-115">-AppSettings</span></span>
<span data-ttu-id="a8afb-116">Azokat a környezeti változókat adja meg, amelyeket a webhely használni fog.</span><span class="sxs-lookup"><span data-stu-id="a8afb-116">Specifies the environment variables that will be used by the website.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8afb-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="a8afb-117">-AutoSwapSlotName</span></span>
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

### <span data-ttu-id="a8afb-118">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="a8afb-118">-ConnectionStrings</span></span>
<span data-ttu-id="a8afb-119">A webhely által használt kapcsolati karakterláncokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8afb-119">Specifies the connection strings used by the website.</span></span>

```yaml
Type: ConnStringPropertyBag
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8afb-120">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="a8afb-120">-DefaultDocuments</span></span>
<span data-ttu-id="a8afb-121">Megadja azokat a dokumentumokat, amelyek automatikusan megjelennek a webhelyen való tallózáskor.</span><span class="sxs-lookup"><span data-stu-id="a8afb-121">Specifies the documents that are automatically displayed when browsing the website.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8afb-122">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="a8afb-122">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="a8afb-123">Meghatározza, hogy a webhelyhez milyen részletes IIS-hibákat naplózjon a rendszer.</span><span class="sxs-lookup"><span data-stu-id="a8afb-123">Determines whether detailed IIS errors are logged for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8afb-124">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="a8afb-124">-HandlerMappings</span></span>
<span data-ttu-id="a8afb-125">A webhely által használt kezelői megfeleltetéseket adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8afb-125">Specifies the handler mappings used by the website.</span></span>

```yaml
Type: HandlerMapping[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8afb-126">-Állomásnevek</span><span class="sxs-lookup"><span data-stu-id="a8afb-126">-HostNames</span></span>
<span data-ttu-id="a8afb-127">A webhely eléréséhez használható teljes tartományneveket adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8afb-127">Specifies the fully qualified host names that can be used to access the website.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8afb-128">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="a8afb-128">-HttpLoggingEnabled</span></span>
<span data-ttu-id="a8afb-129">Meghatározza, hogy engedélyezve van-e a http-naplózás a webhelyen.</span><span class="sxs-lookup"><span data-stu-id="a8afb-129">Determines whether http logging is enabled for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8afb-130">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="a8afb-130">-ManagedPipelineMode</span></span>
<span data-ttu-id="a8afb-131">A felügyelt csővezeték üzemmódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8afb-131">Specifies the managed pipeline mode.</span></span>

```yaml
Type: ManagedPipelineMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8afb-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="a8afb-132">-Metadata</span></span>
<span data-ttu-id="a8afb-133">A webhely metaadatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8afb-133">Specifies the metadata for the website.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.NameValuePair]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8afb-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a8afb-134">-Name</span></span>
<span data-ttu-id="a8afb-135">A webhely nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8afb-135">Specifies the name of the website.</span></span>

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

### <span data-ttu-id="a8afb-136">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="a8afb-136">-NetFrameworkVersion</span></span>
<span data-ttu-id="a8afb-137">A webhely által igényelt .NET-keretrendszer verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8afb-137">Specifies the version of the .Net Framework required by the website.</span></span>

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

### <span data-ttu-id="a8afb-138">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="a8afb-138">-NumberOfWorkers</span></span>
<span data-ttu-id="a8afb-139">A webhelyet futtató munkavégző folyamatok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8afb-139">Specifies the number of worker processes running the website.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8afb-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8afb-140">-PassThru</span></span>
<span data-ttu-id="a8afb-141">Azt jelzi, hogy ez a parancsmag **logikai** értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="a8afb-141">Indicates that this cmdlet returns a **Boolean** value.</span></span>

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

### <span data-ttu-id="a8afb-142">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="a8afb-142">-PhpVersion</span></span>
<span data-ttu-id="a8afb-143">A webhely által igényelt PHP-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8afb-143">Specifies the PHP version required by the website.</span></span>

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

### <span data-ttu-id="a8afb-144">-Profil</span><span class="sxs-lookup"><span data-stu-id="a8afb-144">-Profile</span></span>
<span data-ttu-id="a8afb-145">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="a8afb-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a8afb-146">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="a8afb-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a8afb-147">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="a8afb-147">-RequestTracingEnabled</span></span>
<span data-ttu-id="a8afb-148">Meghatározza, hogy engedélyezve van-e a kérés nyomkövetése a webhelyen.</span><span class="sxs-lookup"><span data-stu-id="a8afb-148">Determines whether request tracing is enabled for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8afb-149">-RoutingRules</span><span class="sxs-lookup"><span data-stu-id="a8afb-149">-RoutingRules</span></span>
<span data-ttu-id="a8afb-150">A termelésben való teszteléshez használandó útválasztási szabályokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8afb-150">Specifies the routing rules to use for testing in production.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.RoutingRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8afb-151">-SiteWithConfig</span><span class="sxs-lookup"><span data-stu-id="a8afb-151">-SiteWithConfig</span></span>
<span data-ttu-id="a8afb-152">A webhely által használt konfigurációt adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8afb-152">Specifies the configuration used by the website.</span></span>

```yaml
Type: SiteWithConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8afb-153">-Slot</span><span class="sxs-lookup"><span data-stu-id="a8afb-153">-Slot</span></span>
<span data-ttu-id="a8afb-154">A webhely tárolóhelyének a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8afb-154">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="a8afb-155">-SlotStickyAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="a8afb-155">-SlotStickyAppSettingNames</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8afb-156">-SlotStickyConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="a8afb-156">-SlotStickyConnectionStringNames</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8afb-157">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="a8afb-157">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="a8afb-158">Megadja, hogy engedélyezve van-e a 32 bites üzemmódja.</span><span class="sxs-lookup"><span data-stu-id="a8afb-158">Specifies whether to enable 32-bit mode.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8afb-159">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="a8afb-159">-WebSocketsEnabled</span></span>
<span data-ttu-id="a8afb-160">Itt adhatja meg, hogy engedélyezi-e a webszoftvercsatornák használatát.</span><span class="sxs-lookup"><span data-stu-id="a8afb-160">Specifies whether to enable WebSockets.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8afb-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8afb-161">CommonParameters</span></span>
<span data-ttu-id="a8afb-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8afb-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8afb-163">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8afb-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8afb-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8afb-164">INPUTS</span></span>

## <span data-ttu-id="a8afb-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8afb-165">OUTPUTS</span></span>

## <span data-ttu-id="a8afb-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8afb-166">NOTES</span></span>

## <span data-ttu-id="a8afb-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8afb-167">RELATED LINKS</span></span>

[<span data-ttu-id="a8afb-168">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a8afb-168">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="a8afb-169">Új – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a8afb-169">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="a8afb-170">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a8afb-170">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)


