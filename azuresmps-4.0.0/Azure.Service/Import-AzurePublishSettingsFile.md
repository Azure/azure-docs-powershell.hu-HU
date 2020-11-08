---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 79D64D7C-6671-4F03-8776-70A716F36512
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bc0525ee7238de421842b74f52f7dd4fa59df1a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016261"
---
# <span data-ttu-id="159fb-101">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="159fb-101">Import-AzurePublishSettingsFile</span></span>

## <span data-ttu-id="159fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="159fb-102">SYNOPSIS</span></span>
<span data-ttu-id="159fb-103">Importálja a közzétételi beállításokat tartalmazó fájlt, amely lehetővé teszi az Azure-fiókok kezelését a Windows PowerShellben.</span><span class="sxs-lookup"><span data-stu-id="159fb-103">Imports a publish settings file that lets you manage your Azure accounts in Windows PowerShell.</span></span>

## <span data-ttu-id="159fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="159fb-104">SYNTAX</span></span>

```
Import-AzurePublishSettingsFile -PublishSettingsFile <String> [-Environment <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="159fb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="159fb-105">DESCRIPTION</span></span>
<span data-ttu-id="159fb-106">Az **import-AzurePublishSettingsFile** parancsmag olyan közzétételi beállításokat tartalmazó fájlt (\*. publishsettings) importál, amely információkat tartalmaz az Azure-fiókokról, és az előfizetési adatfájlt menti a számítógépre.</span><span class="sxs-lookup"><span data-stu-id="159fb-106">The **Import-AzurePublishSettingsFile** cmdlet imports a publish settings file (\*.publishsettings) that contains information about your Azure accounts and saves a subscription data file on your computer.</span></span>
<span data-ttu-id="159fb-107">A parancsmag befejezésekor az Azure-fiókok kezelése a Windows PowerShellben végezhető el.</span><span class="sxs-lookup"><span data-stu-id="159fb-107">When the cmdlet completes, you can manage your Azure accounts in Windows PowerShell.</span></span>

<span data-ttu-id="159fb-108">Mielőtt futtatná az **importálási AzurePublishSettingsFile** , futtassa a **Get-AzurePublishSettingsFile** , amely letölti és menti a közzétételi beállításokat tartalmazó fájlt, így importálhatja.</span><span class="sxs-lookup"><span data-stu-id="159fb-108">Before running **Import-AzurePublishSettingsFile** , run **Get-AzurePublishSettingsFile** , which downloads and saves the publish settings file so you can import it.</span></span>

<span data-ttu-id="159fb-109">Ha az Azure-fiókját elérhetővé szeretné tenni a Windows PowerShellben, használhatja a közzétételi beállításokat tartalmazó fájlt vagy az **Add-AzureAccount** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="159fb-109">To make your Azure account available to Windows PowerShell, you can use a publish settings file or the **Add-AzureAccount** cmdlet.</span></span>
<span data-ttu-id="159fb-110">A beállítási fájlok közzététele lehetővé teszi, hogy a munkamenetet előre felkészítse, így a parancsfájlok és a háttérben végzett feladatok felügyelet nélkül is használhatók.</span><span class="sxs-lookup"><span data-stu-id="159fb-110">Publish settings files let you prepare the session in advance so you can run scripts and background jobs unattended.</span></span>
<span data-ttu-id="159fb-111">Nem minden szolgáltatás támogatja a közzétételi beállítások fájljait.</span><span class="sxs-lookup"><span data-stu-id="159fb-111">However, not all services support publish settings files.</span></span>
<span data-ttu-id="159fb-112">A **AzureResourceManager** modul például nem támogatja a közzétételi beállítások fájljait.</span><span class="sxs-lookup"><span data-stu-id="159fb-112">For example, the **AzureResourceManager** module does not support publish settings files.</span></span>

<span data-ttu-id="159fb-113">**Biztonsági Megjegyzés:** A közzétételi beállítások fájljai olyan felügyeleti tanúsítványokat tartalmaznak, amelyek kódoltak, de nem titkosítottak.</span><span class="sxs-lookup"><span data-stu-id="159fb-113">**Security Note:** Publish settings files contain a management certificate that is encoded, but not encrypted.</span></span>
<span data-ttu-id="159fb-114">Ha a rosszindulatú felhasználók hozzáférhetnek a közzétételi beállítási fájlhoz, az Azure-szolgáltatások szerkeszthetők, hozhatók létre és törölhetők.</span><span class="sxs-lookup"><span data-stu-id="159fb-114">If  malicious users access your publish settings file,  they might be able to edit, create, and delete your Azure services.</span></span>
<span data-ttu-id="159fb-115">Biztonsági szempontból célszerű lehet menteni a fájlt a letöltések vagy a dokumentumok mappa egy helyére, majd az **import-AzurePublishSettingsFile** parancsmag használatával importálja a beállításokat.</span><span class="sxs-lookup"><span data-stu-id="159fb-115">As a security best practice, save the file to a location in your Downloads or Documents folder and then delete it after using **Import-AzurePublishSettingsFile** cmdlet to import the settings.</span></span>

## <span data-ttu-id="159fb-116">Példák</span><span class="sxs-lookup"><span data-stu-id="159fb-116">EXAMPLES</span></span>

### <span data-ttu-id="159fb-117">1. példa: fájl importálása</span><span class="sxs-lookup"><span data-stu-id="159fb-117">Example 1: Import a file</span></span>
```
PS C:\> Import-AzurePublishSettingsFile -PublishSettingsFile C:\Temp\MyAccount.publishsettings
```

<span data-ttu-id="159fb-118">A parancs a "C:\Temp\MyAccount.publishsettings" fájlt importálja.</span><span class="sxs-lookup"><span data-stu-id="159fb-118">This command imports the "C:\Temp\MyAccount.publishsettings" file.</span></span>

## <span data-ttu-id="159fb-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="159fb-119">PARAMETERS</span></span>

### <span data-ttu-id="159fb-120">-Környezet</span><span class="sxs-lookup"><span data-stu-id="159fb-120">-Environment</span></span>
<span data-ttu-id="159fb-121">Azure-környezetet ad meg.</span><span class="sxs-lookup"><span data-stu-id="159fb-121">Specifies an Azure environment.</span></span>

<span data-ttu-id="159fb-122">Azure-környezet: a Microsoft Azure független központi üzembe állítása, például a AzureCloud a globális Azure-és a AzureChinaCloud által üzemeltetett Azure-alapú 21Vianet Kínában.</span><span class="sxs-lookup"><span data-stu-id="159fb-122">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="159fb-123">A helyszíni Azure-környezeteket az Azure Pack és a WAPack parancsmagok használatával is létrehozhatja.</span><span class="sxs-lookup"><span data-stu-id="159fb-123">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="159fb-124">További tudnivalókat az [Azure Pack (csomag](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ) című témakörben talál https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="159fb-124">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="159fb-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="159fb-125">-Profile</span></span>
<span data-ttu-id="159fb-126">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="159fb-126">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="159fb-127">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="159fb-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="159fb-128">-PublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="159fb-128">-PublishSettingsFile</span></span>
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

### <span data-ttu-id="159fb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="159fb-129">CommonParameters</span></span>
<span data-ttu-id="159fb-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="159fb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="159fb-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="159fb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="159fb-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="159fb-132">INPUTS</span></span>

### <span data-ttu-id="159fb-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="159fb-133">None</span></span>
<span data-ttu-id="159fb-134">A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="159fb-134">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="159fb-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="159fb-135">OUTPUTS</span></span>

### <span data-ttu-id="159fb-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="159fb-136">None</span></span>
<span data-ttu-id="159fb-137">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="159fb-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="159fb-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="159fb-138">NOTES</span></span>
* <span data-ttu-id="159fb-139">A "közzétételi beállítások fájl" egy. publishsettings fájlnév-kiterjesztésű XML-fájl.</span><span class="sxs-lookup"><span data-stu-id="159fb-139">A "publish settings file" is an XML file with a .publishsettings file name extension.</span></span> <span data-ttu-id="159fb-140">A fájl olyan kódolt tanúsítványt tartalmaz, amely felügyeleti hitelesítő adatokat biztosít az Azure-előfizetésekhez.</span><span class="sxs-lookup"><span data-stu-id="159fb-140">The file contains an encoded certificate that provides management credentials for your Azure subscriptions.</span></span> <span data-ttu-id="159fb-141">A fájl importálása után törölje azt a biztonsági kockázatok elkerülése érdekében.</span><span class="sxs-lookup"><span data-stu-id="159fb-141">After you import this file, delete it to avoid security risks.</span></span>
* <span data-ttu-id="159fb-142">Az "előfizetés-adatfájl" olyan XML-fájl, amelyet a számítógépére biztonságosan lehet menteni.</span><span class="sxs-lookup"><span data-stu-id="159fb-142">A "subscription data file" is an XML file that can be saved on your computer safely.</span></span> <span data-ttu-id="159fb-143">Alapértelmezés szerint a rendszer a központi felhasználói profilba menti a fájlt ($home/AppData/Roaming).</span><span class="sxs-lookup"><span data-stu-id="159fb-143">By default, it's saved in your roaming user profile ($home/AppData/Roaming).</span></span>

## <span data-ttu-id="159fb-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="159fb-144">RELATED LINKS</span></span>

[<span data-ttu-id="159fb-145">Az Azure PowerShell telepítése és beállítása</span><span class="sxs-lookup"><span data-stu-id="159fb-145">How to Install and Configure Azure PowerShell</span></span>](https://azure.microsoft.com/documentation/articles/install-configure-powershell/)

[<span data-ttu-id="159fb-146">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="159fb-146">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="159fb-147">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="159fb-147">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)


