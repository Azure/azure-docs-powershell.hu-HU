---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 9595E785-6DBF-433C-83B3-8506A3B49B13
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 242dfd46b179d1e7d55613d938eddf5b691da6c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680223"
---
# <span data-ttu-id="d1315-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="d1315-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="d1315-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d1315-102">SYNOPSIS</span></span>
<span data-ttu-id="d1315-103">Megkapja a webhely-helyreállítási Vault beállítási fájlját.</span><span class="sxs-lookup"><span data-stu-id="d1315-103">Gets the Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1315-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d1315-104">SYNTAX</span></span>

### <span data-ttu-id="d1315-105">ByParam (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d1315-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1315-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="d1315-106">Default</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1315-107">ForSite</span><span class="sxs-lookup"><span data-stu-id="d1315-107">ForSite</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> -SiteIdentifier <String> -SiteFriendlyName <String>
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1315-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d1315-108">DESCRIPTION</span></span>
<span data-ttu-id="d1315-109">A **Get-AzureRmSiteRecoveryVaultSettingsFile** parancsmag az Azure-webhely helyreállítási boltozatának beállítási fájlját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d1315-109">The **Get-AzureRmSiteRecoveryVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="d1315-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d1315-110">EXAMPLES</span></span>

## <span data-ttu-id="d1315-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d1315-111">PARAMETERS</span></span>

### <span data-ttu-id="d1315-112">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="d1315-112">-Path</span></span>
<span data-ttu-id="d1315-113">A webhely-helyreállítási boltozat beállítási fájljának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1315-113">Specifies the path to the Site Recovery vault settings file.</span></span>
<span data-ttu-id="d1315-114">Ha helyileg szeretné menteni a fájlt, töltse le a webhely-helyreállítási központ portálról a parancs befejezését követően.</span><span class="sxs-lookup"><span data-stu-id="d1315-114">To store this file locally, download it from the Site Recovery vault portal once the command completes.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, ForSite
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1315-115">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d1315-115">-SiteFriendlyName</span></span>
<span data-ttu-id="d1315-116">Annak a helynek a neve, amely a boltozatot akkor adja meg, ha a webhely Hyper-V-webhelye.</span><span class="sxs-lookup"><span data-stu-id="d1315-116">Specifies the site friendly name for the vault when the site is a Hyper-V site.</span></span>

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

### <span data-ttu-id="d1315-117">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="d1315-117">-SiteIdentifier</span></span>
<span data-ttu-id="d1315-118">Annak a helynek az azonosítóját adja meg a boltozatnak, amikor a webhely Hyper-V-webhely.</span><span class="sxs-lookup"><span data-stu-id="d1315-118">Specifies the site identifier for the vault when the site is a Hyper-V site.</span></span>

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

### <span data-ttu-id="d1315-119">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="d1315-119">-Vault</span></span>
<span data-ttu-id="d1315-120">A webhely boltozat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1315-120">Specifies the vault object for the site.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVault
Parameter Sets: Default, ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1315-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1315-121">-DefaultProfile</span></span>
<span data-ttu-id="d1315-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d1315-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1315-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1315-123">CommonParameters</span></span>
<span data-ttu-id="d1315-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d1315-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1315-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1315-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1315-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1315-126">INPUTS</span></span>

### <span data-ttu-id="d1315-127">ASRVault</span><span class="sxs-lookup"><span data-stu-id="d1315-127">ASRVault</span></span>
<span data-ttu-id="d1315-128">A "Vault" paraméter az "ASRVault" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d1315-128">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="d1315-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1315-129">OUTPUTS</span></span>

### <span data-ttu-id="d1315-130">Microsoft. Azure. Command. SiteRecovery. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="d1315-130">Microsoft.Azure.Commands.SiteRecovery.VaultSettingsFilePath</span></span>

## <span data-ttu-id="d1315-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d1315-131">NOTES</span></span>

## <span data-ttu-id="d1315-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1315-132">RELATED LINKS</span></span>

[<span data-ttu-id="d1315-133">Importálás – AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="d1315-133">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureRmSiteRecoveryVaultSettingsFile.md)

[<span data-ttu-id="d1315-134">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="d1315-134">Set-AzureRmSiteRecoveryVaultSettings</span></span>](./Set-AzureRmSiteRecoveryVaultSettings.md)
