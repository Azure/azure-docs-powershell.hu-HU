---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 070DA86E-9EA4-4777-9D53-64B58B4401B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 42863e0dbf6982ced1f77f916c97ed4fc19d6979
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503936"
---
# <span data-ttu-id="c9f59-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="c9f59-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="c9f59-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9f59-102">SYNOPSIS</span></span>
<span data-ttu-id="c9f59-103">Webhely-helyreállítási Vault-beállítási fájl importálása</span><span class="sxs-lookup"><span data-stu-id="c9f59-103">Imports a Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9f59-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9f59-104">SYNTAX</span></span>

```
Import-AzureRmSiteRecoveryVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9f59-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9f59-105">DESCRIPTION</span></span>
<span data-ttu-id="c9f59-106">Az **import-AzureRmSiteRecoveryVaultSettingsFile** parancsmag az Azure webhely-helyreállítási tároló beállítási fájljába importálja az aktuális munkamenetben az azt követő helyreállítási műveletekhez tartozó Vault-környezet beállítását.</span><span class="sxs-lookup"><span data-stu-id="c9f59-106">The **Import-AzureRmSiteRecoveryVaultSettingsFile** cmdlet imports an Azure Site Recovery vault settings file to set the vault context for subsequent Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="c9f59-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c9f59-107">EXAMPLES</span></span>

## <span data-ttu-id="c9f59-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9f59-108">PARAMETERS</span></span>

### <span data-ttu-id="c9f59-109">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="c9f59-109">-Path</span></span>
<span data-ttu-id="c9f59-110">A webhely-helyreállítási boltozat beállítási fájljának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9f59-110">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="c9f59-111">Ez a fájl letölthető a webhely-helyreállítási Vault portálról, és helyben tárolható.</span><span class="sxs-lookup"><span data-stu-id="c9f59-111">This file can be downloaded from the Site Recovery vault portal and stored locally.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9f59-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9f59-112">-DefaultProfile</span></span>
<span data-ttu-id="c9f59-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9f59-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9f59-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9f59-114">CommonParameters</span></span>
<span data-ttu-id="c9f59-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9f59-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9f59-116">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9f59-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9f59-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9f59-117">INPUTS</span></span>

## <span data-ttu-id="c9f59-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9f59-118">OUTPUTS</span></span>

### <span data-ttu-id="c9f59-119">Microsoft. Azure. Command. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="c9f59-119">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="c9f59-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9f59-120">NOTES</span></span>

## <span data-ttu-id="c9f59-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9f59-121">RELATED LINKS</span></span>

[<span data-ttu-id="c9f59-122">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="c9f59-122">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureRmSiteRecoveryVaultSettingsFile.md)
