---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: 603cd65195f9e33c5006dcb4f2dc98ffc64aa7a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501655"
---
# <span data-ttu-id="96345-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="96345-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="96345-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96345-102">SYNOPSIS</span></span>
<span data-ttu-id="96345-103">Megkapja az Azure webhely-helyreállítási Vault beállítási fájlját.</span><span class="sxs-lookup"><span data-stu-id="96345-103">Gets the Azure Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96345-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96345-104">SYNTAX</span></span>

### <span data-ttu-id="96345-105">ForSite</span><span class="sxs-lookup"><span data-stu-id="96345-105">ForSite</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="96345-106">ByDefault</span><span class="sxs-lookup"><span data-stu-id="96345-106">ByDefault</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96345-107">ForBackupVaultType</span><span class="sxs-lookup"><span data-stu-id="96345-107">ForBackupVaultType</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96345-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="96345-108">DESCRIPTION</span></span>
<span data-ttu-id="96345-109">A **Get-AzureRmRecoveryServicesVaultSettingsFile** parancsmag az Azure-webhely helyreállítási boltozatának beállítási fájlját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="96345-109">The **Get-AzureRmRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="96345-110">Példák</span><span class="sxs-lookup"><span data-stu-id="96345-110">EXAMPLES</span></span>

### <span data-ttu-id="96345-111">1. példa: Windows Server-vagy DPM-gép regisztrálása az Azure Backup szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="96345-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="96345-112">Az első parancs a TestVault nevű boltozatot kapja, majd a $Vault 01 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="96345-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>

<span data-ttu-id="96345-113">A második parancs beállítja a $CredsPath változót a C:\Downloads.-ra.</span><span class="sxs-lookup"><span data-stu-id="96345-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>

<span data-ttu-id="96345-114">Az utolsó parancs az Azure biztonsági másolat $CredsPath hitelesítő adataival kapja meg $Vault 01 rendszerhez tartozó Vault hitelesítő adatait tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="96345-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

## <span data-ttu-id="96345-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96345-115">PARAMETERS</span></span>

### <span data-ttu-id="96345-116">-Backup</span><span class="sxs-lookup"><span data-stu-id="96345-116">-Backup</span></span>
<span data-ttu-id="96345-117">Jelzi, hogy a Vault hitelesítőadat-fájl az Azure Backup alkalmazásra érvényes.</span><span class="sxs-lookup"><span data-stu-id="96345-117">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

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

### <span data-ttu-id="96345-118">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="96345-118">-Path</span></span>
<span data-ttu-id="96345-119">Az Azure webhely-helyreállítási Vault-beállítások fájljának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="96345-119">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="96345-120">Ezt a fájlt az Azure site Recovery Vault portálról töltheti le, és helyileg tárolhatja.</span><span class="sxs-lookup"><span data-stu-id="96345-120">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

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

### <span data-ttu-id="96345-121">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="96345-121">-SiteFriendlyName</span></span>
<span data-ttu-id="96345-122">A webhely felhasználóbarát nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="96345-122">Specifies the site friendly name.</span></span>
<span data-ttu-id="96345-123">Akkor használja ezt a paramétert, ha a Hyper-V-webhelyhez tartozó Vault-hitelesítő adatokat tölti le.</span><span class="sxs-lookup"><span data-stu-id="96345-123">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="96345-124">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="96345-124">-SiteIdentifier</span></span>
<span data-ttu-id="96345-125">A webhely azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="96345-125">Specifies the site identifier.</span></span>
<span data-ttu-id="96345-126">Akkor használja ezt a paramétert, ha a Hyper-V-webhelyhez tartozó Vault-hitelesítő adatokat tölti le.</span><span class="sxs-lookup"><span data-stu-id="96345-126">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="96345-127">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="96345-127">-SiteRecovery</span></span>
<span data-ttu-id="96345-128">Jelzi, hogy a Vault hitelesítőadat-fájl az Azure-webhely helyreállítása esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="96345-128">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

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

### <span data-ttu-id="96345-129">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="96345-129">-Vault</span></span>
<span data-ttu-id="96345-130">Az Azure webhely-helyreállítási boltozat objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="96345-130">Specifies the Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="96345-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96345-131">-DefaultProfile</span></span>
<span data-ttu-id="96345-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96345-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96345-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96345-133">CommonParameters</span></span>
<span data-ttu-id="96345-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96345-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96345-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96345-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96345-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96345-136">INPUTS</span></span>

### <span data-ttu-id="96345-137">ARSVault</span><span class="sxs-lookup"><span data-stu-id="96345-137">ARSVault</span></span>
<span data-ttu-id="96345-138">A "Vault" paraméter az "ARSVault" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="96345-138">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="96345-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96345-139">OUTPUTS</span></span>

### <span data-ttu-id="96345-140">Microsoft. Azure. Command. RecoveryServices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="96345-140">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="96345-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96345-141">NOTES</span></span>

## <span data-ttu-id="96345-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96345-142">RELATED LINKS</span></span>

[<span data-ttu-id="96345-143">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="96345-143">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="96345-144">Új – AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="96345-144">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="96345-145">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="96345-145">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


