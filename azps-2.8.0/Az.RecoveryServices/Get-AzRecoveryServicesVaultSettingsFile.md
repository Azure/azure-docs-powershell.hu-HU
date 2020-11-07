---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: 5455babba58e050397066e5439b3e046315b4101
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838563"
---
# <span data-ttu-id="02b1f-101">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="02b1f-101">Get-AzRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="02b1f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="02b1f-102">SYNOPSIS</span></span>
<span data-ttu-id="02b1f-103">Megkapja az Azure webhely-helyreállítási Vault beállítási fájlját.</span><span class="sxs-lookup"><span data-stu-id="02b1f-103">Gets the Azure Site Recovery vault settings file.</span></span>

## <span data-ttu-id="02b1f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="02b1f-104">SYNTAX</span></span>

### <span data-ttu-id="02b1f-105">ForSiteWithCertificate</span><span class="sxs-lookup"><span data-stu-id="02b1f-105">ForSiteWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -SiteIdentifier <String>
 -Certificate <String> -SiteFriendlyName <String> [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="02b1f-106">ByDefaultWithCertificate</span><span class="sxs-lookup"><span data-stu-id="02b1f-106">ByDefaultWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String>
 [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02b1f-107">ForBackupVaultTypeWithCertificate</span><span class="sxs-lookup"><span data-stu-id="02b1f-107">ForBackupVaultTypeWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String> [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02b1f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="02b1f-108">DESCRIPTION</span></span>
<span data-ttu-id="02b1f-109">A **Get-AzRecoveryServicesVaultSettingsFile** parancsmag az Azure-webhely helyreállítási boltozatának beállítási fájlját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="02b1f-109">The **Get-AzRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="02b1f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="02b1f-110">EXAMPLES</span></span>

### <span data-ttu-id="02b1f-111">1. példa: Windows Server-vagy DPM-gép regisztrálása az Azure Backup szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="02b1f-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="02b1f-112">Az első parancs a TestVault nevű boltozatot kapja, majd a $Vault 01 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="02b1f-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="02b1f-113">A második parancs beállítja a $CredsPath változót a C:\Downloads.-ra.</span><span class="sxs-lookup"><span data-stu-id="02b1f-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="02b1f-114">Az utolsó parancs az Azure biztonsági másolat $CredsPath hitelesítő adataival kapja meg $Vault 01 rendszerhez tartozó Vault hitelesítő adatait tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="02b1f-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="02b1f-115">2. példa:</span><span class="sxs-lookup"><span data-stu-id="02b1f-115">Example 2:</span></span>
```
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="02b1f-116">A parancs beolvassa a Vault hitelesítő adatait tartalmazó fájlt $Vault 01 a Vault típusú siteRecovery.</span><span class="sxs-lookup"><span data-stu-id="02b1f-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="02b1f-117">3. példa: Windows Server-vagy DPM-gép regisztrálása az Azure Backup szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="02b1f-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="02b1f-118">A parancs a $Vault 01-es számú Vault hitelesítő adatait tartalmazó fájlt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="02b1f-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="02b1f-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="02b1f-119">PARAMETERS</span></span>

### <span data-ttu-id="02b1f-120">-Backup</span><span class="sxs-lookup"><span data-stu-id="02b1f-120">-Backup</span></span>
<span data-ttu-id="02b1f-121">Jelzi, hogy a Vault hitelesítőadat-fájl az Azure Backup alkalmazásra érvényes.</span><span class="sxs-lookup"><span data-stu-id="02b1f-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

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

### <span data-ttu-id="02b1f-122">-Tanúsítvány</span><span class="sxs-lookup"><span data-stu-id="02b1f-122">-Certificate</span></span>
<span data-ttu-id="02b1f-123">{{Kitöltési tanúsítvány leírása}}</span><span class="sxs-lookup"><span data-stu-id="02b1f-123">{{Fill Certificate Description}}</span></span>

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

### <span data-ttu-id="02b1f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02b1f-124">-DefaultProfile</span></span>
<span data-ttu-id="02b1f-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02b1f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02b1f-126">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="02b1f-126">-Path</span></span>
<span data-ttu-id="02b1f-127">Az Azure webhely-helyreállítási Vault-beállítások fájljának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="02b1f-127">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="02b1f-128">Ezt a fájlt az Azure site Recovery Vault portálról töltheti le, és helyileg tárolhatja.</span><span class="sxs-lookup"><span data-stu-id="02b1f-128">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

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

### <span data-ttu-id="02b1f-129">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="02b1f-129">-SiteFriendlyName</span></span>
<span data-ttu-id="02b1f-130">A webhely felhasználóbarát nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="02b1f-130">Specifies the site friendly name.</span></span>
<span data-ttu-id="02b1f-131">Akkor használja ezt a paramétert, ha a Hyper-V-webhelyhez tartozó Vault-hitelesítő adatokat tölti le.</span><span class="sxs-lookup"><span data-stu-id="02b1f-131">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="02b1f-132">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="02b1f-132">-SiteIdentifier</span></span>
<span data-ttu-id="02b1f-133">A webhely azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="02b1f-133">Specifies the site identifier.</span></span>
<span data-ttu-id="02b1f-134">Akkor használja ezt a paramétert, ha a Hyper-V-webhelyhez tartozó Vault-hitelesítő adatokat tölti le.</span><span class="sxs-lookup"><span data-stu-id="02b1f-134">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="02b1f-135">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="02b1f-135">-SiteRecovery</span></span>
<span data-ttu-id="02b1f-136">Jelzi, hogy a Vault hitelesítőadat-fájl az Azure-webhely helyreállítása esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="02b1f-136">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

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

### <span data-ttu-id="02b1f-137">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="02b1f-137">-Vault</span></span>
<span data-ttu-id="02b1f-138">Az Azure webhely-helyreállítási boltozat objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="02b1f-138">Specifies the Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="02b1f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02b1f-139">CommonParameters</span></span>
<span data-ttu-id="02b1f-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="02b1f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02b1f-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02b1f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02b1f-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="02b1f-142">INPUTS</span></span>

### <span data-ttu-id="02b1f-143">Microsoft. Azure. Command. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="02b1f-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="02b1f-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02b1f-144">OUTPUTS</span></span>

### <span data-ttu-id="02b1f-145">Microsoft. Azure. Command. RecoveryServices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="02b1f-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="02b1f-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="02b1f-146">NOTES</span></span>

## <span data-ttu-id="02b1f-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02b1f-147">RELATED LINKS</span></span>

[<span data-ttu-id="02b1f-148">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="02b1f-148">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="02b1f-149">Új – AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="02b1f-149">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="02b1f-150">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="02b1f-150">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


