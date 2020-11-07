---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: ad22cbe1cb17e69358ef386b478fe929abe415b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672425"
---
# <span data-ttu-id="13d2e-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="13d2e-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="13d2e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13d2e-102">SYNOPSIS</span></span>
<span data-ttu-id="13d2e-103">Importálja a megadott ASR-tároló beállítási fájlját a boltozat környezetének (PowerShell-munkamenet-környezet) beállításához a PowerShell-munkamenetben a további ASR-műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="13d2e-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13d2e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13d2e-104">SYNTAX</span></span>

```
Import-AzureRmRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13d2e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="13d2e-105">DESCRIPTION</span></span>
<span data-ttu-id="13d2e-106">Az **import-AzureRmRecoveryServicesAsrVaultSettingsFile** parancsmag importálja az Azure-webhely helyreállítási Vault-beállításait tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="13d2e-106">The **Import-AzureRmRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="13d2e-107">A Vault-beállítások fájl az aktuális munkamenetben a következő Azure-webhely-helyreállítási műveletek boltozat-környezetének beállítására szolgál.</span><span class="sxs-lookup"><span data-stu-id="13d2e-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="13d2e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="13d2e-108">EXAMPLES</span></span>

### <span data-ttu-id="13d2e-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="13d2e-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzureRmRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="13d2e-110">Importálja a megadott helyreállítási szolgáltatások Vault-beállítási fájlját, és az importált boltozat beállításait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="13d2e-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="13d2e-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13d2e-111">PARAMETERS</span></span>

### <span data-ttu-id="13d2e-112">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="13d2e-112">-Path</span></span>
<span data-ttu-id="13d2e-113">Az ASR-boltozat beállítási fájljának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="13d2e-113">Specifies the path of the ASR vault settings file.</span></span>
<span data-ttu-id="13d2e-114">Ez a fájl letölthető a helyreállítási szolgáltatások Vault-portálról, és helyben tárolható.</span><span class="sxs-lookup"><span data-stu-id="13d2e-114">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

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

### <span data-ttu-id="13d2e-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="13d2e-115">-Confirm</span></span>
<span data-ttu-id="13d2e-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="13d2e-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13d2e-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13d2e-117">-WhatIf</span></span>
<span data-ttu-id="13d2e-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="13d2e-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13d2e-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="13d2e-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13d2e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13d2e-120">CommonParameters</span></span>
<span data-ttu-id="13d2e-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="13d2e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13d2e-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13d2e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13d2e-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13d2e-123">INPUTS</span></span>

### <span data-ttu-id="13d2e-124">System. String</span><span class="sxs-lookup"><span data-stu-id="13d2e-124">System.String</span></span>

## <span data-ttu-id="13d2e-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13d2e-125">OUTPUTS</span></span>

### <span data-ttu-id="13d2e-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="13d2e-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="13d2e-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13d2e-127">NOTES</span></span>

## <span data-ttu-id="13d2e-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13d2e-128">RELATED LINKS</span></span>

[<span data-ttu-id="13d2e-129">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="13d2e-129">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesAsrVaultSettingsFile.md)
