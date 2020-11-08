---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AFAA1BDF-3F6A-437A-ADC2-C5EBD970F57D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e86fdb7f1e995af71e09bdce17754b11819bec
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016564"
---
# <span data-ttu-id="379c1-101">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="379c1-101">Get-AzureSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="379c1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="379c1-102">SYNOPSIS</span></span>
<span data-ttu-id="379c1-103">Megkapja a webhely-helyreállítási Vault beállítási fájlját.</span><span class="sxs-lookup"><span data-stu-id="379c1-103">Gets the Site Recovery vault settings file.</span></span>

## <span data-ttu-id="379c1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="379c1-104">SYNTAX</span></span>

### <span data-ttu-id="379c1-105">ByParam (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="379c1-105">ByParam (Default)</span></span>
```
Get-AzureSiteRecoveryVaultSettingsFile -Name <String> -Location <String> [-SiteName <String>]
 [-SiteId <String>] [-Path <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="379c1-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="379c1-106">ByObject</span></span>
```
Get-AzureSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Site <ASRSite>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="379c1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="379c1-107">DESCRIPTION</span></span>
<span data-ttu-id="379c1-108">A **Get-AzureSiteRecoveryVaultSettingsFile** parancsmag az Azure-webhely helyreállítási boltozatának beállítási fájlját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="379c1-108">The **Get-AzureSiteRecoveryVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="379c1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="379c1-109">EXAMPLES</span></span>

### <span data-ttu-id="379c1-110">Példa 1: a beállítások fájl beszerzése egy boltozathoz</span><span class="sxs-lookup"><span data-stu-id="379c1-110">Example 1: Get the settings file for a vault</span></span>
```
PS C:\> $Vault = Get-AzureSiteRecoveryVault -Name "ContosoVault"
PS C:\> Get-AzureSiteRecoveryVaultSettingsFile -Vault $Vault
FilePath 
-------- 
C:\Users\ContosoAdmin\ContosoVault_2015-02-02T05-39-23.VaultCredentials
```

<span data-ttu-id="379c1-111">Az első parancs a **Get-AzureSiteRecoveryVault** parancsmaggal kapja meg a ContosoVault nevű aktív Azure site Recovery Vault nevet.</span><span class="sxs-lookup"><span data-stu-id="379c1-111">The first command gets the active Azure Site Recovery vault named ContosoVault by using the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>
<span data-ttu-id="379c1-112">A parancs a $Vault változóban tárolja a boltozatot.</span><span class="sxs-lookup"><span data-stu-id="379c1-112">The command stores that vault in the $Vault variable.</span></span>

<span data-ttu-id="379c1-113">A második parancs beolvassa a $Vault-ban tárolt Vault-tároló beállítási fájlját.</span><span class="sxs-lookup"><span data-stu-id="379c1-113">The second command gets the settings file for the vault stored in $Vault.</span></span>

## <span data-ttu-id="379c1-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="379c1-114">PARAMETERS</span></span>

### <span data-ttu-id="379c1-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="379c1-115">-Location</span></span>
<span data-ttu-id="379c1-116">Azt a földrajzi helyet adja meg, ahová a boltozat tartozik.</span><span class="sxs-lookup"><span data-stu-id="379c1-116">Specifies the geographical location to which the vault belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="379c1-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="379c1-117">-Name</span></span>
<span data-ttu-id="379c1-118">A boltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="379c1-118">Specifies the name of a vault.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="379c1-119">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="379c1-119">-Path</span></span>
<span data-ttu-id="379c1-120">A webhely-helyreállítási boltozat beállítási fájljának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="379c1-120">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="379c1-121">Ha helyileg szeretné menteni a fájlt, töltse le a webhely-helyreállítási központ webhelyről a parancs futásának befejezése után.</span><span class="sxs-lookup"><span data-stu-id="379c1-121">To store this file locally, download it from the Site Recovery vault portal after the command has finished running.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="379c1-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="379c1-122">-Profile</span></span>
<span data-ttu-id="379c1-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="379c1-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="379c1-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="379c1-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="379c1-125">-Webhely</span><span class="sxs-lookup"><span data-stu-id="379c1-125">-Site</span></span>
<span data-ttu-id="379c1-126">Itt adhatja meg azt a webhelyet, amelyhez beállítási fájlt szeretne beszerezni.</span><span class="sxs-lookup"><span data-stu-id="379c1-126">Specifies a site for which to get a settings file.</span></span>
<span data-ttu-id="379c1-127">Ha egy **webhely** -objektumot szeretne beolvasni, használja a **Get-AzureSiteRecoverySite** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="379c1-127">To obtain a **Site** object, use the **Get-AzureSiteRecoverySite** cmdlet.</span></span>

```yaml
Type: ASRSite
Parameter Sets: ByObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="379c1-128">-Helyazonosító</span><span class="sxs-lookup"><span data-stu-id="379c1-128">-SiteId</span></span>
<span data-ttu-id="379c1-129">Egy webhely AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="379c1-129">Specifies the ID of a site.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="379c1-130">-SiteName</span><span class="sxs-lookup"><span data-stu-id="379c1-130">-SiteName</span></span>
<span data-ttu-id="379c1-131">A webhely nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="379c1-131">Specifies the name of a site.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="379c1-132">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="379c1-132">-Vault</span></span>
<span data-ttu-id="379c1-133">A webhely boltozatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="379c1-133">Specifies the vault for the site.</span></span>

```yaml
Type: ASRVault
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="379c1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="379c1-134">CommonParameters</span></span>
<span data-ttu-id="379c1-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="379c1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="379c1-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="379c1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="379c1-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="379c1-137">INPUTS</span></span>

## <span data-ttu-id="379c1-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="379c1-138">OUTPUTS</span></span>

## <span data-ttu-id="379c1-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="379c1-139">NOTES</span></span>

## <span data-ttu-id="379c1-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="379c1-140">RELATED LINKS</span></span>

[<span data-ttu-id="379c1-141">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="379c1-141">Get-AzureSiteRecoverySite</span></span>](./Get-AzureSiteRecoverySite.md)

[<span data-ttu-id="379c1-142">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="379c1-142">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="379c1-143">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="379c1-143">Get-AzureSiteRecoveryVaultSettings</span></span>](./Get-AzureSiteRecoveryVaultSettings.md)

[<span data-ttu-id="379c1-144">Importálás – AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="379c1-144">Import-AzureSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureSiteRecoveryVaultSettingsFile.md)


