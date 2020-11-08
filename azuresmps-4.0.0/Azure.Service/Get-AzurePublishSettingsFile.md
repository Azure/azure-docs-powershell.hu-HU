---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: A5419F76-B85E-445D-84EA-CC695B175C8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1364cf1bbec1fdca2a8c9901556d38de0b620358
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015633"
---
# <span data-ttu-id="d8456-101">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="d8456-101">Get-AzurePublishSettingsFile</span></span>

## <span data-ttu-id="d8456-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d8456-102">SYNOPSIS</span></span>
<span data-ttu-id="d8456-103">Az Azure-előfizetés közzétételi beállítások fájljának letöltése.</span><span class="sxs-lookup"><span data-stu-id="d8456-103">Downloads the publish settings file for an Azure subscription.</span></span>

## <span data-ttu-id="d8456-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d8456-104">SYNTAX</span></span>

```
Get-AzurePublishSettingsFile [-Environment <String>] [-Realm <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8456-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d8456-105">DESCRIPTION</span></span>
<span data-ttu-id="d8456-106">A **Get-AzurePublishSettingsFile** parancsmag letölti az előfizetéshez tartozó közzétételi beállítások fájlt a fiókjába.</span><span class="sxs-lookup"><span data-stu-id="d8456-106">The **Get-AzurePublishSettingsFile** cmdlet downloads a publish settings file for a subscription in your account.</span></span>
<span data-ttu-id="d8456-107">Ha befejeződött a parancs, az **import-PublishSettingsFile** parancsmaggal megadhatja, hogy a fájl beállításai elérhetők legyenek a Windows PowerShellben.</span><span class="sxs-lookup"><span data-stu-id="d8456-107">When the command completes, you can use the **Import-PublishSettingsFile** cmdlet to make the settings in the file available to Windows PowerShell.</span></span>

<span data-ttu-id="d8456-108">Ha az Azure-fiókját elérhetővé szeretné tenni a Windows PowerShellben, használhatja a közzétételi beállításokat tartalmazó fájlt vagy az **Add-AzureAccount** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d8456-108">To make your Azure account available to Windows PowerShell, you can use a publish settings file or the **Add-AzureAccount** cmdlet.</span></span>
<span data-ttu-id="d8456-109">A beállítási fájlok közzététele lehetővé teszi, hogy a munkamenetet előre felkészítse, így a parancsfájlok és a háttérben végzett feladatok felügyelet nélkül is használhatók.</span><span class="sxs-lookup"><span data-stu-id="d8456-109">Publish settings files let you prepare the session in advance so you can run scripts and background jobs unattended.</span></span>
<span data-ttu-id="d8456-110">Nem minden szolgáltatás támogatja a közzétételi beállítások fájljait.</span><span class="sxs-lookup"><span data-stu-id="d8456-110">However, not all services support publish settings files.</span></span>
<span data-ttu-id="d8456-111">A **AzureResourceManager** modul például nem támogatja a közzétételi beállítások fájljait.</span><span class="sxs-lookup"><span data-stu-id="d8456-111">For example, the **AzureResourceManager** module does not support publish settings files.</span></span>

<span data-ttu-id="d8456-112">A **Get-AzurePublishSettingsFile** futtatásakor megnyílik az alapértelmezett böngésző, és kéri, hogy lépjen be az Azure-fiókjába, jelölje ki az előfizetést, és válassza ki a fájl rendszerhelyét a közzétételi beállítások fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="d8456-112">When you run **Get-AzurePublishSettingsFile** , it opens your default browser and prompts you to sign into your Azure account, select a subscription, and select a file system location for the publish settings file.</span></span>
<span data-ttu-id="d8456-113">Ezután letölti az előfizetéshez tartozó közzétételi beállítások fájlt a kijelölt fájlba.</span><span class="sxs-lookup"><span data-stu-id="d8456-113">Then, it downloads the publish settings file for your subscription into the file that you selected.</span></span>

<span data-ttu-id="d8456-114">A "közzétételi beállítások fájl" egy. publishsettings fájlnév-kiterjesztésű XML-fájl.</span><span class="sxs-lookup"><span data-stu-id="d8456-114">A "publish settings file" is an XML file with a .publishsettings file name extension.</span></span>
<span data-ttu-id="d8456-115">A fájl olyan kódolt tanúsítványt tartalmaz, amely felügyeleti hitelesítő adatokat biztosít az Azure-előfizetésekhez.</span><span class="sxs-lookup"><span data-stu-id="d8456-115">The file contains an encoded certificate that provides management credentials for your Azure subscriptions.</span></span>

<span data-ttu-id="d8456-116">**Biztonsági Megjegyzés:** A közzétételi beállítások fájljai az Azure-előfizetések és-szolgáltatások felügyeletéhez használt hitelesítő adatokat tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="d8456-116">**Security Note:** Publish settings files contains credentials that are used to administer your Azure subscriptions and services.</span></span>
<span data-ttu-id="d8456-117">Ha a rosszindulatú felhasználók hozzáférhetnek a közzétételi beállítási fájlhoz, szerkeszthetik, hozhatják létre és törölhetik az Azure-szolgáltatásokat.</span><span class="sxs-lookup"><span data-stu-id="d8456-117">If  malicious users access your publish settings file,  they can edit, create, and delete your Azure services.</span></span>
<span data-ttu-id="d8456-118">Biztonsági szempontból célszerű lehet menteni a fájlt a letöltések vagy a dokumentumok mappa egy helyére, majd az **import-AzurePublishSettingsFile** parancsmag használatával importálja a beállításokat.</span><span class="sxs-lookup"><span data-stu-id="d8456-118">As a security best practice, save the file to a location in your Downloads or Documents folder and then delete it after using **Import-AzurePublishSettingsFile** cmdlet to import the settings.</span></span>

<span data-ttu-id="d8456-119">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="d8456-119">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d8456-120">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d8456-120">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="d8456-121">Példák</span><span class="sxs-lookup"><span data-stu-id="d8456-121">EXAMPLES</span></span>

### <span data-ttu-id="d8456-122">Példa 1: a közzétételi beállítások fájl letöltése</span><span class="sxs-lookup"><span data-stu-id="d8456-122">Example 1: Download a publish settings file</span></span>
```
PS C:\> Get-AzurePublishSettingsFile
```

<span data-ttu-id="d8456-123">Ez a parancs megnyitja az alapértelmezett böngészőt, csatlakozik a Windows Azure-fiókjához, majd letölti a fiókjához tartozó. publishsettings fájlt.</span><span class="sxs-lookup"><span data-stu-id="d8456-123">This command opens your default browser, connects to your Windows Azure account, and then downloads the .publishsettings file for your account.</span></span>

### <span data-ttu-id="d8456-124">2. példa: a tartomány megadása</span><span class="sxs-lookup"><span data-stu-id="d8456-124">Example 2: Specify a realm</span></span>
```
PS C:\> Get-AzurePublishSettingsFile -Realm contoso.com -Passthru
```

<span data-ttu-id="d8456-125">Ez a parancs letölti a contoso.com tartományban lévő fiókhoz tartozó közzétételi beállítások fájlt.</span><span class="sxs-lookup"><span data-stu-id="d8456-125">This command downloads the publish settings file for an account in the contoso.com domain.</span></span>
<span data-ttu-id="d8456-126">Ha az Azure-ba egy Microsoft-fiók helyett szervezeti fiókkal jelentkezik be, használja a **tartomány** paramétert tartalmazó parancsot.</span><span class="sxs-lookup"><span data-stu-id="d8456-126">Use a command with the **Realm** parameter when you sign into Azure with an organizational account, instead of a Microsoft account.</span></span>

## <span data-ttu-id="d8456-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d8456-127">PARAMETERS</span></span>

### <span data-ttu-id="d8456-128">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d8456-128">-Environment</span></span>
<span data-ttu-id="d8456-129">Azure-környezetet ad meg.</span><span class="sxs-lookup"><span data-stu-id="d8456-129">Specifies an Azure environment.</span></span>

<span data-ttu-id="d8456-130">Azure-környezet: a Microsoft Azure független központi üzembe állítása, például a AzureCloud a globális Azure-és a AzureChinaCloud által üzemeltetett Azure-alapú 21Vianet Kínában.</span><span class="sxs-lookup"><span data-stu-id="d8456-130">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="d8456-131">A helyszíni Azure-környezeteket az Azure Pack és a WAPack parancsmagok használatával is létrehozhatja.</span><span class="sxs-lookup"><span data-stu-id="d8456-131">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="d8456-132">További tudnivalókat az [Azure Pack (csomag](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ) című témakörben talál https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d8456-132">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="d8456-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8456-133">-PassThru</span></span>
<span data-ttu-id="d8456-134">A parancs eredményét $True, ha a parancs sikerül, és a $False sikertelen.</span><span class="sxs-lookup"><span data-stu-id="d8456-134">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="d8456-135">Ez a parancsmag alapértelmezés szerint nem ad vissza semmilyen eredményt.</span><span class="sxs-lookup"><span data-stu-id="d8456-135">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="d8456-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="d8456-136">-Profile</span></span>
<span data-ttu-id="d8456-137">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d8456-137">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d8456-138">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d8456-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d8456-139">-Realm</span><span class="sxs-lookup"><span data-stu-id="d8456-139">-Realm</span></span>
<span data-ttu-id="d8456-140">A szervezeti AZONOSÍTÓban lévő szervezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="d8456-140">Specifies the organization in an organizational ID.</span></span>
<span data-ttu-id="d8456-141">Ha például az Azure as-be jelentkezik be admin@contoso.com , a **tartomány** paraméter értéke contoso.com.</span><span class="sxs-lookup"><span data-stu-id="d8456-141">For example, if you sign into Azure as admin@contoso.com, the value of the **Realm** parameter is contoso.com.</span></span>
<span data-ttu-id="d8456-142">Akkor használja ezt a paramétert, ha szervezeti AZONOSÍTÓval jelentkezik be az Azure-portálra.</span><span class="sxs-lookup"><span data-stu-id="d8456-142">Use this parameter when you use an organizational ID to sign into the Azure portal.</span></span>
<span data-ttu-id="d8456-143">Ez a paraméter a Microsoft-fiók (például outlook.com-vagy live.com-fiók) használata esetén nem szükséges.</span><span class="sxs-lookup"><span data-stu-id="d8456-143">This parameter is not required when you use a Microsoft account, such as an outlook.com or live.com account.</span></span>

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

### <span data-ttu-id="d8456-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8456-144">CommonParameters</span></span>
<span data-ttu-id="d8456-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d8456-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8456-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8456-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8456-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8456-147">INPUTS</span></span>

### <span data-ttu-id="d8456-148">Nincs</span><span class="sxs-lookup"><span data-stu-id="d8456-148">None</span></span>
<span data-ttu-id="d8456-149">A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="d8456-149">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="d8456-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8456-150">OUTPUTS</span></span>

### <span data-ttu-id="d8456-151">Nincs vagy System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d8456-151">None or System.Boolean</span></span>
<span data-ttu-id="d8456-152">A *PassThru* paraméter használatakor ez a parancsmag logikai értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="d8456-152">When you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="d8456-153">Ellenkező esetben ez a parancsmag nem adja vissza a kimenetet</span><span class="sxs-lookup"><span data-stu-id="d8456-153">Otherwise, this cmdlet does not return any output</span></span>

## <span data-ttu-id="d8456-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d8456-154">NOTES</span></span>

## <span data-ttu-id="d8456-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8456-155">RELATED LINKS</span></span>

[<span data-ttu-id="d8456-156">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="d8456-156">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="d8456-157">Importálás – AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="d8456-157">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)


