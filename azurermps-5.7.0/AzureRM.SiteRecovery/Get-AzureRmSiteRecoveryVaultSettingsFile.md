---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 9595E785-6DBF-433C-83B3-8506A3B49B13
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 621e5ac05c5f975ff3878781bcb8c5a1b40c04bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679681"
---
# <span data-ttu-id="8ba83-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="8ba83-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="8ba83-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8ba83-102">SYNOPSIS</span></span>
<span data-ttu-id="8ba83-103">Megkapja a webhely-helyreállítási Vault beállítási fájlját.</span><span class="sxs-lookup"><span data-stu-id="8ba83-103">Gets the Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ba83-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8ba83-104">SYNTAX</span></span>

### <span data-ttu-id="8ba83-105">ByParam (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8ba83-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ba83-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="8ba83-106">Default</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ba83-107">ForSite</span><span class="sxs-lookup"><span data-stu-id="8ba83-107">ForSite</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> -SiteIdentifier <String> -SiteFriendlyName <String>
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ba83-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8ba83-108">DESCRIPTION</span></span>
<span data-ttu-id="8ba83-109">A **Get-AzureRmSiteRecoveryVaultSettingsFile** parancsmag az Azure-webhely helyreállítási boltozatának beállítási fájlját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8ba83-109">The **Get-AzureRmSiteRecoveryVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="8ba83-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8ba83-110">EXAMPLES</span></span>

## <span data-ttu-id="8ba83-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8ba83-111">PARAMETERS</span></span>

### <span data-ttu-id="8ba83-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ba83-112">-DefaultProfile</span></span>
<span data-ttu-id="8ba83-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8ba83-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ba83-114">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="8ba83-114">-Path</span></span>
<span data-ttu-id="8ba83-115">A webhely-helyreállítási boltozat beállítási fájljának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8ba83-115">Specifies the path to the Site Recovery vault settings file.</span></span>
<span data-ttu-id="8ba83-116">Ha helyileg szeretné menteni a fájlt, töltse le a webhely-helyreállítási központ portálról a parancs befejezését követően.</span><span class="sxs-lookup"><span data-stu-id="8ba83-116">To store this file locally, download it from the Site Recovery vault portal once the command completes.</span></span>

```yaml
Type: String
Parameter Sets: Default, ForSite
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba83-117">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="8ba83-117">-SiteFriendlyName</span></span>
<span data-ttu-id="8ba83-118">Annak a helynek a neve, amely a boltozatot akkor adja meg, ha a webhely Hyper-V-webhelye.</span><span class="sxs-lookup"><span data-stu-id="8ba83-118">Specifies the site friendly name for the vault when the site is a Hyper-V site.</span></span>

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

### <span data-ttu-id="8ba83-119">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="8ba83-119">-SiteIdentifier</span></span>
<span data-ttu-id="8ba83-120">Annak a helynek az azonosítóját adja meg a boltozatnak, amikor a webhely Hyper-V-webhely.</span><span class="sxs-lookup"><span data-stu-id="8ba83-120">Specifies the site identifier for the vault when the site is a Hyper-V site.</span></span>

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

### <span data-ttu-id="8ba83-121">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="8ba83-121">-Vault</span></span>
<span data-ttu-id="8ba83-122">A webhely boltozat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8ba83-122">Specifies the vault object for the site.</span></span>

```yaml
Type: ASRVault
Parameter Sets: Default, ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba83-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ba83-123">CommonParameters</span></span>
<span data-ttu-id="8ba83-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8ba83-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ba83-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ba83-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ba83-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ba83-126">INPUTS</span></span>

### <span data-ttu-id="8ba83-127">ASRVault</span><span class="sxs-lookup"><span data-stu-id="8ba83-127">ASRVault</span></span>
<span data-ttu-id="8ba83-128">A "Vault" paraméter az "ASRVault" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8ba83-128">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="8ba83-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ba83-129">OUTPUTS</span></span>

### <span data-ttu-id="8ba83-130">Microsoft. Azure. Command. SiteRecovery. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="8ba83-130">Microsoft.Azure.Commands.SiteRecovery.VaultSettingsFilePath</span></span>

## <span data-ttu-id="8ba83-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8ba83-131">NOTES</span></span>

## <span data-ttu-id="8ba83-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ba83-132">RELATED LINKS</span></span>

[<span data-ttu-id="8ba83-133">Importálás – AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="8ba83-133">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureRmSiteRecoveryVaultSettingsFile.md)

[<span data-ttu-id="8ba83-134">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="8ba83-134">Set-AzureRmSiteRecoveryVaultSettings</span></span>](./Set-AzureRmSiteRecoveryVaultSettings.md)
