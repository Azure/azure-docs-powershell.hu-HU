---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: 0d074c18ad9b5f9ea34a465acd4a91a88d4b69ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160154"
---
# <span data-ttu-id="ca816-101">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="ca816-101">Get-AzRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="ca816-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca816-102">SYNOPSIS</span></span>
<span data-ttu-id="ca816-103">Lekérte az Azure Site Recovery tároló beállításfájlját.</span><span class="sxs-lookup"><span data-stu-id="ca816-103">Gets the Azure Site Recovery vault settings file.</span></span>

## <span data-ttu-id="ca816-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ca816-104">SYNTAX</span></span>

### <span data-ttu-id="ca816-105">ForSiteWithCertificate</span><span class="sxs-lookup"><span data-stu-id="ca816-105">ForSiteWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -SiteIdentifier <String>
 -Certificate <String> -SiteFriendlyName <String> [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ca816-106">ByDefaultWithCertificate</span><span class="sxs-lookup"><span data-stu-id="ca816-106">ByDefaultWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String>
 [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca816-107">ForBackupVaultTypeWithCertificate</span><span class="sxs-lookup"><span data-stu-id="ca816-107">ForBackupVaultTypeWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String> [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca816-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ca816-108">DESCRIPTION</span></span>
<span data-ttu-id="ca816-109">A **Get-AzRecoveryServicesVaultSettingsFile** parancsmag az Azure Webhely-helyreállítási tároló beállításfájlját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ca816-109">The **Get-AzRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="ca816-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ca816-110">EXAMPLES</span></span>

### <span data-ttu-id="ca816-111">1. példa: Windows Server- vagy DPM-gép regisztrálása az Azure biztonsági mentéséhez</span><span class="sxs-lookup"><span data-stu-id="ca816-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```powershell
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="ca816-112">Az első parancs megkapja a TestVault nevű tárolót, majd a $Vault 01 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ca816-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="ca816-113">A második parancs a $CredsPath C:\Letöltések változót állítja be.</span><span class="sxs-lookup"><span data-stu-id="ca816-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="ca816-114">Az utolsó parancs az Azure biztonsági másolat $Vault 01 tároló hitelesítő adatait $CredsPath le.</span><span class="sxs-lookup"><span data-stu-id="ca816-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="ca816-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="ca816-115">Example 2</span></span>
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="ca816-116">A parancs lekérte a $Vault 01 tároló típusú siteRecovery fájlját.</span><span class="sxs-lookup"><span data-stu-id="ca816-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="ca816-117">3. példa: Windows Server- vagy DPM-gép regisztrálása az Azure biztonsági mentéséhez</span><span class="sxs-lookup"><span data-stu-id="ca816-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="ca816-118">A parancs lekérte a tároló hitelesítő adatait a $Vault 01-hez.</span><span class="sxs-lookup"><span data-stu-id="ca816-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="ca816-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca816-119">PARAMETERS</span></span>

### <span data-ttu-id="ca816-120">-Backup</span><span class="sxs-lookup"><span data-stu-id="ca816-120">-Backup</span></span>
<span data-ttu-id="ca816-121">Azt jelzi, hogy a tároló hitelesítőadat-fájlja érvényes az Azure Biztonsági mentésre.</span><span class="sxs-lookup"><span data-stu-id="ca816-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultTypeWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca816-122">-Certificate</span><span class="sxs-lookup"><span data-stu-id="ca816-122">-Certificate</span></span>
<span data-ttu-id="ca816-123">{{Fill Certificate Description}}</span><span class="sxs-lookup"><span data-stu-id="ca816-123">{{Fill Certificate Description}}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca816-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca816-124">-DefaultProfile</span></span>
<span data-ttu-id="ca816-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ca816-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca816-126">-Path</span><span class="sxs-lookup"><span data-stu-id="ca816-126">-Path</span></span>
<span data-ttu-id="ca816-127">Az Azure Site Recovery tárolóbeállítási fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ca816-127">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="ca816-128">Ezt a fájlt letöltheti az Azure Site Recovery tároló portálról, és helyben tárolhatja.</span><span class="sxs-lookup"><span data-stu-id="ca816-128">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca816-129">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="ca816-129">-SiteFriendlyName</span></span>
<span data-ttu-id="ca816-130">A webhely felhasználóbarát nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ca816-130">Specifies the site friendly name.</span></span>
<span data-ttu-id="ca816-131">Akkor használja ezt a paramétert, ha egy Hyper-V-webhely hitelesítő adatait töltse le.</span><span class="sxs-lookup"><span data-stu-id="ca816-131">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca816-132">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="ca816-132">-SiteIdentifier</span></span>
<span data-ttu-id="ca816-133">Megadja a webhely azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="ca816-133">Specifies the site identifier.</span></span>
<span data-ttu-id="ca816-134">Akkor használja ezt a paramétert, ha egy Hyper-V-webhely hitelesítő adatait töltse le.</span><span class="sxs-lookup"><span data-stu-id="ca816-134">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca816-135">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ca816-135">-SiteRecovery</span></span>
<span data-ttu-id="ca816-136">Azt jelzi, hogy a tároló hitelesítőadat-fájlja érvényes az Azure-webhely-helyreállításra.</span><span class="sxs-lookup"><span data-stu-id="ca816-136">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSiteWithCertificate, ByDefaultWithCertificate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca816-137">-Vault</span><span class="sxs-lookup"><span data-stu-id="ca816-137">-Vault</span></span>
<span data-ttu-id="ca816-138">Az Azure Site Recovery tároló objektumát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="ca816-138">Specifies the Azure Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca816-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca816-139">CommonParameters</span></span>
<span data-ttu-id="ca816-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca816-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca816-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca816-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca816-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca816-142">INPUTS</span></span>

### <span data-ttu-id="ca816-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="ca816-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="ca816-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca816-144">OUTPUTS</span></span>

### <span data-ttu-id="ca816-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="ca816-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="ca816-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ca816-146">NOTES</span></span>

## <span data-ttu-id="ca816-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca816-147">RELATED LINKS</span></span>

[<span data-ttu-id="ca816-148">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ca816-148">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="ca816-149">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ca816-149">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="ca816-150">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ca816-150">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


