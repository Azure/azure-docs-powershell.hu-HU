---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 070DA86E-9EA4-4777-9D53-64B58B4401B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/import-azurermsiterecoveryvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 11233414250377331f75e3e8b69f262a0f3a0537
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502383"
---
# <span data-ttu-id="5e3d6-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="5e3d6-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="5e3d6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5e3d6-102">SYNOPSIS</span></span>
<span data-ttu-id="5e3d6-103">Webhely-helyreállítási Vault-beállítási fájl importálása</span><span class="sxs-lookup"><span data-stu-id="5e3d6-103">Imports a Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e3d6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5e3d6-104">SYNTAX</span></span>

```
Import-AzureRmSiteRecoveryVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e3d6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5e3d6-105">DESCRIPTION</span></span>
<span data-ttu-id="5e3d6-106">Az **import-AzureRmSiteRecoveryVaultSettingsFile** parancsmag az Azure webhely-helyreállítási tároló beállítási fájljába importálja az aktuális munkamenetben az azt követő helyreállítási műveletekhez tartozó Vault-környezet beállítását.</span><span class="sxs-lookup"><span data-stu-id="5e3d6-106">The **Import-AzureRmSiteRecoveryVaultSettingsFile** cmdlet imports an Azure Site Recovery vault settings file to set the vault context for subsequent Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="5e3d6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5e3d6-107">EXAMPLES</span></span>

## <span data-ttu-id="5e3d6-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5e3d6-108">PARAMETERS</span></span>

### <span data-ttu-id="5e3d6-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e3d6-109">-DefaultProfile</span></span>
<span data-ttu-id="5e3d6-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5e3d6-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e3d6-111">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="5e3d6-111">-Path</span></span>
<span data-ttu-id="5e3d6-112">A webhely-helyreállítási boltozat beállítási fájljának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5e3d6-112">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="5e3d6-113">Ez a fájl letölthető a webhely-helyreállítási Vault portálról, és helyben tárolható.</span><span class="sxs-lookup"><span data-stu-id="5e3d6-113">This file can be downloaded from the Site Recovery vault portal and stored locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e3d6-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e3d6-114">CommonParameters</span></span>
<span data-ttu-id="5e3d6-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5e3d6-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e3d6-116">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e3d6-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e3d6-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e3d6-117">INPUTS</span></span>

### <span data-ttu-id="5e3d6-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="5e3d6-118">None</span></span>
<span data-ttu-id="5e3d6-119">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="5e3d6-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5e3d6-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e3d6-120">OUTPUTS</span></span>

### <span data-ttu-id="5e3d6-121">Microsoft. Azure. Command. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="5e3d6-121">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="5e3d6-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5e3d6-122">NOTES</span></span>

## <span data-ttu-id="5e3d6-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e3d6-123">RELATED LINKS</span></span>

[<span data-ttu-id="5e3d6-124">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="5e3d6-124">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureRmSiteRecoveryVaultSettingsFile.md)
