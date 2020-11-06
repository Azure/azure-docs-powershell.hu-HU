---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: a0572e73d270a37b3c705018a38b4a88fe88d1e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503435"
---
# <span data-ttu-id="d66dd-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="d66dd-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="d66dd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d66dd-102">SYNOPSIS</span></span>
<span data-ttu-id="d66dd-103">Megkapja az Azure webhely-helyreállítási Vault beállítási fájlját.</span><span class="sxs-lookup"><span data-stu-id="d66dd-103">Gets the Azure Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d66dd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d66dd-104">SYNTAX</span></span>

### <span data-ttu-id="d66dd-105">ForSite</span><span class="sxs-lookup"><span data-stu-id="d66dd-105">ForSite</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d66dd-106">ByDefault</span><span class="sxs-lookup"><span data-stu-id="d66dd-106">ByDefault</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d66dd-107">ForBackupVaultType</span><span class="sxs-lookup"><span data-stu-id="d66dd-107">ForBackupVaultType</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d66dd-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d66dd-108">DESCRIPTION</span></span>
<span data-ttu-id="d66dd-109">A **Get-AzureRmRecoveryServicesVaultSettingsFile** parancsmag az Azure-webhely helyreállítási boltozatának beállítási fájlját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d66dd-109">The **Get-AzureRmRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="d66dd-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d66dd-110">EXAMPLES</span></span>

### <span data-ttu-id="d66dd-111">1. példa: Windows Server-vagy DPM-gép regisztrálása az Azure Backup szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="d66dd-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="d66dd-112">Az első parancs a TestVault nevű boltozatot kapja, majd a $Vault 01 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d66dd-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="d66dd-113">A második parancs beállítja a $CredsPath változót a C:\Downloads.-ra.</span><span class="sxs-lookup"><span data-stu-id="d66dd-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="d66dd-114">Az utolsó parancs az Azure biztonsági másolat $CredsPath hitelesítő adataival kapja meg $Vault 01 rendszerhez tartozó Vault hitelesítő adatait tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="d66dd-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="d66dd-115">2. példa:</span><span class="sxs-lookup"><span data-stu-id="d66dd-115">Example 2:</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="d66dd-116">A parancs beolvassa a Vault hitelesítő adatait tartalmazó fájlt $Vault 01 a Vault típusú siteRecovery.</span><span class="sxs-lookup"><span data-stu-id="d66dd-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="d66dd-117">3. példa: Windows Server-vagy DPM-gép regisztrálása az Azure Backup szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="d66dd-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="d66dd-118">A parancs a $Vault 01-es számú Vault hitelesítő adatait tartalmazó fájlt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d66dd-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="d66dd-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d66dd-119">PARAMETERS</span></span>

### <span data-ttu-id="d66dd-120">-Backup</span><span class="sxs-lookup"><span data-stu-id="d66dd-120">-Backup</span></span>
<span data-ttu-id="d66dd-121">Jelzi, hogy a Vault hitelesítőadat-fájl az Azure Backup alkalmazásra érvényes.</span><span class="sxs-lookup"><span data-stu-id="d66dd-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66dd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d66dd-122">-DefaultProfile</span></span>
<span data-ttu-id="d66dd-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d66dd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66dd-124">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="d66dd-124">-Path</span></span>
<span data-ttu-id="d66dd-125">Az Azure webhely-helyreállítási Vault-beállítások fájljának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d66dd-125">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="d66dd-126">Ezt a fájlt az Azure site Recovery Vault portálról töltheti le, és helyileg tárolhatja.</span><span class="sxs-lookup"><span data-stu-id="d66dd-126">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

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

### <span data-ttu-id="d66dd-127">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d66dd-127">-SiteFriendlyName</span></span>
<span data-ttu-id="d66dd-128">A webhely felhasználóbarát nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d66dd-128">Specifies the site friendly name.</span></span>
<span data-ttu-id="d66dd-129">Akkor használja ezt a paramétert, ha a Hyper-V-webhelyhez tartozó Vault-hitelesítő adatokat tölti le.</span><span class="sxs-lookup"><span data-stu-id="d66dd-129">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66dd-130">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="d66dd-130">-SiteIdentifier</span></span>
<span data-ttu-id="d66dd-131">A webhely azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d66dd-131">Specifies the site identifier.</span></span>
<span data-ttu-id="d66dd-132">Akkor használja ezt a paramétert, ha a Hyper-V-webhelyhez tartozó Vault-hitelesítő adatokat tölti le.</span><span class="sxs-lookup"><span data-stu-id="d66dd-132">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66dd-133">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="d66dd-133">-SiteRecovery</span></span>
<span data-ttu-id="d66dd-134">Jelzi, hogy a Vault hitelesítőadat-fájl az Azure-webhely helyreállítása esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="d66dd-134">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSite, ByDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66dd-135">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="d66dd-135">-Vault</span></span>
<span data-ttu-id="d66dd-136">Az Azure webhely-helyreállítási boltozat objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d66dd-136">Specifies the Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="d66dd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d66dd-137">CommonParameters</span></span>
<span data-ttu-id="d66dd-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d66dd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d66dd-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d66dd-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d66dd-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d66dd-140">INPUTS</span></span>

### <span data-ttu-id="d66dd-141">Microsoft. Azure. Command. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="d66dd-141">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="d66dd-142">Paraméterek: Vault (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d66dd-142">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="d66dd-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d66dd-143">OUTPUTS</span></span>

### <span data-ttu-id="d66dd-144">Microsoft. Azure. Command. RecoveryServices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="d66dd-144">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="d66dd-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d66dd-145">NOTES</span></span>

## <span data-ttu-id="d66dd-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d66dd-146">RELATED LINKS</span></span>

[<span data-ttu-id="d66dd-147">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="d66dd-147">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="d66dd-148">Új – AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="d66dd-148">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="d66dd-149">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="d66dd-149">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


