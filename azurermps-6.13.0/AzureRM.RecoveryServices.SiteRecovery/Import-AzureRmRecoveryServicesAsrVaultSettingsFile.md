---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/import-azurermrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: 7bb92a55f366d90eb5993cfe1520d1b516214372
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492795"
---
# <span data-ttu-id="7338f-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="7338f-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="7338f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7338f-102">SYNOPSIS</span></span>
<span data-ttu-id="7338f-103">Importálja a megadott ASR-tároló beállítási fájlját a boltozat környezetének (PowerShell-munkamenet-környezet) beállításához a PowerShell-munkamenetben a további ASR-műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="7338f-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7338f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7338f-104">SYNTAX</span></span>

```
Import-AzureRmRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7338f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7338f-105">DESCRIPTION</span></span>
<span data-ttu-id="7338f-106">Az **import-AzureRmRecoveryServicesAsrVaultSettingsFile** parancsmag importálja az Azure-webhely helyreállítási Vault-beállításait tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="7338f-106">The **Import-AzureRmRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="7338f-107">A Vault-beállítások fájl az aktuális munkamenetben a következő Azure-webhely-helyreállítási műveletek boltozat-környezetének beállítására szolgál.</span><span class="sxs-lookup"><span data-stu-id="7338f-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="7338f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="7338f-108">EXAMPLES</span></span>

### <span data-ttu-id="7338f-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7338f-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzureRmRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="7338f-110">Importálja a megadott helyreállítási szolgáltatások Vault-beállítási fájlját, és az importált boltozat beállításait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7338f-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="7338f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7338f-111">PARAMETERS</span></span>

### <span data-ttu-id="7338f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7338f-112">-DefaultProfile</span></span>
<span data-ttu-id="7338f-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7338f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7338f-114">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="7338f-114">-Path</span></span>
<span data-ttu-id="7338f-115">Az ASR-Vault beállítási fájl mappájának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7338f-115">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="7338f-116">Ez a fájl letölthető a helyreállítási szolgáltatások Vault-portálról, és helyben tárolható.</span><span class="sxs-lookup"><span data-stu-id="7338f-116">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

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

### <span data-ttu-id="7338f-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7338f-117">-Confirm</span></span>
<span data-ttu-id="7338f-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7338f-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7338f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7338f-119">-WhatIf</span></span>
<span data-ttu-id="7338f-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7338f-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7338f-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7338f-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7338f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7338f-122">CommonParameters</span></span>
<span data-ttu-id="7338f-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7338f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7338f-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7338f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7338f-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7338f-125">INPUTS</span></span>

### <span data-ttu-id="7338f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7338f-126">System.String</span></span>

## <span data-ttu-id="7338f-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7338f-127">OUTPUTS</span></span>

### <span data-ttu-id="7338f-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="7338f-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="7338f-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7338f-129">NOTES</span></span>

## <span data-ttu-id="7338f-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7338f-130">RELATED LINKS</span></span>

[<span data-ttu-id="7338f-131">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="7338f-131">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesAsrVaultSettingsFile.md)
