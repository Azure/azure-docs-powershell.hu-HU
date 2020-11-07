---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: b272f22c0bac37f5318deff50f1f0b56a849ce2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679268"
---
# <span data-ttu-id="c0a88-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="c0a88-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="c0a88-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c0a88-102">SYNOPSIS</span></span>
<span data-ttu-id="c0a88-103">Megkapja az Azure webhely-helyreállítási Vault beállítási fájlját.</span><span class="sxs-lookup"><span data-stu-id="c0a88-103">Gets the Azure Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0a88-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c0a88-104">SYNTAX</span></span>

### <span data-ttu-id="c0a88-105">ForSite</span><span class="sxs-lookup"><span data-stu-id="c0a88-105">ForSite</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0a88-106">ByDefault</span><span class="sxs-lookup"><span data-stu-id="c0a88-106">ByDefault</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0a88-107">ForBackupVaultType</span><span class="sxs-lookup"><span data-stu-id="c0a88-107">ForBackupVaultType</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0a88-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c0a88-108">DESCRIPTION</span></span>
<span data-ttu-id="c0a88-109">A **Get-AzureRmRecoveryServicesVaultSettingsFile** parancsmag az Azure-webhely helyreállítási boltozatának beállítási fájlját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c0a88-109">The **Get-AzureRmRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="c0a88-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c0a88-110">EXAMPLES</span></span>

### <span data-ttu-id="c0a88-111">1. példa: Windows Server-vagy DPM-gép regisztrálása az Azure Backup szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="c0a88-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="c0a88-112">Az első parancs a TestVault nevű boltozatot kapja, majd a $Vault 01 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c0a88-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>

<span data-ttu-id="c0a88-113">A második parancs beállítja a $CredsPath változót a C:\Downloads.-ra.</span><span class="sxs-lookup"><span data-stu-id="c0a88-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>

<span data-ttu-id="c0a88-114">Az utolsó parancs az Azure biztonsági másolat $CredsPath hitelesítő adataival kapja meg $Vault 01 rendszerhez tartozó Vault hitelesítő adatait tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="c0a88-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="c0a88-115">2. példa:</span><span class="sxs-lookup"><span data-stu-id="c0a88-115">Example 2:</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="c0a88-116">A parancs beolvassa a Vault hitelesítő adatait tartalmazó fájlt $Vault 01 a Vault típusú siteRecovery.</span><span class="sxs-lookup"><span data-stu-id="c0a88-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="c0a88-117">3. példa: Windows Server-vagy DPM-gép regisztrálása az Azure Backup szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="c0a88-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="c0a88-118">A parancs a $Vault 01-es számú Vault hitelesítő adatait tartalmazó fájlt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c0a88-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="c0a88-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c0a88-119">PARAMETERS</span></span>

### <span data-ttu-id="c0a88-120">-Backup</span><span class="sxs-lookup"><span data-stu-id="c0a88-120">-Backup</span></span>
<span data-ttu-id="c0a88-121">Jelzi, hogy a Vault hitelesítőadat-fájl az Azure Backup alkalmazásra érvényes.</span><span class="sxs-lookup"><span data-stu-id="c0a88-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForBackupVaultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0a88-122">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="c0a88-122">-Path</span></span>
<span data-ttu-id="c0a88-123">Az Azure webhely-helyreállítási Vault-beállítások fájljának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0a88-123">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="c0a88-124">Ezt a fájlt az Azure site Recovery Vault portálról töltheti le, és helyileg tárolhatja.</span><span class="sxs-lookup"><span data-stu-id="c0a88-124">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0a88-125">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="c0a88-125">-SiteFriendlyName</span></span>
<span data-ttu-id="c0a88-126">A webhely felhasználóbarát nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0a88-126">Specifies the site friendly name.</span></span>
<span data-ttu-id="c0a88-127">Akkor használja ezt a paramétert, ha a Hyper-V-webhelyhez tartozó Vault-hitelesítő adatokat tölti le.</span><span class="sxs-lookup"><span data-stu-id="c0a88-127">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0a88-128">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="c0a88-128">-SiteIdentifier</span></span>
<span data-ttu-id="c0a88-129">A webhely azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0a88-129">Specifies the site identifier.</span></span>
<span data-ttu-id="c0a88-130">Akkor használja ezt a paramétert, ha a Hyper-V-webhelyhez tartozó Vault-hitelesítő adatokat tölti le.</span><span class="sxs-lookup"><span data-stu-id="c0a88-130">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0a88-131">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c0a88-131">-SiteRecovery</span></span>
<span data-ttu-id="c0a88-132">Jelzi, hogy a Vault hitelesítőadat-fájl az Azure-webhely helyreállítása esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="c0a88-132">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForSite, ByDefault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0a88-133">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="c0a88-133">-Vault</span></span>
<span data-ttu-id="c0a88-134">Az Azure webhely-helyreállítási boltozat objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0a88-134">Specifies the Azure Site Recovery vault object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0a88-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0a88-135">-DefaultProfile</span></span>
<span data-ttu-id="c0a88-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0a88-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0a88-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0a88-137">CommonParameters</span></span>
<span data-ttu-id="c0a88-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c0a88-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0a88-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0a88-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0a88-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0a88-140">INPUTS</span></span>

### <span data-ttu-id="c0a88-141">ARSVault</span><span class="sxs-lookup"><span data-stu-id="c0a88-141">ARSVault</span></span>
<span data-ttu-id="c0a88-142">A "Vault" paraméter az "ARSVault" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="c0a88-142">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="c0a88-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0a88-143">OUTPUTS</span></span>

### <span data-ttu-id="c0a88-144">Microsoft. Azure. Command. RecoveryServices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="c0a88-144">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="c0a88-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c0a88-145">NOTES</span></span>

## <span data-ttu-id="c0a88-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0a88-146">RELATED LINKS</span></span>

[<span data-ttu-id="c0a88-147">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="c0a88-147">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="c0a88-148">Új – AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="c0a88-148">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="c0a88-149">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="c0a88-149">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


