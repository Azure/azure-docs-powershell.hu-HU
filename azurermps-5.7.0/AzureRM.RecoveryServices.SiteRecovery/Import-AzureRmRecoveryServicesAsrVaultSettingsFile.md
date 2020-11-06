---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/import-azurermrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: ef92265a59271e321f9e2002e75cb4ea9d64542d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498896"
---
# <span data-ttu-id="1b9aa-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="1b9aa-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="1b9aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1b9aa-102">SYNOPSIS</span></span>
<span data-ttu-id="1b9aa-103">Importálja a megadott ASR-tároló beállítási fájlját a boltozat környezetének (PowerShell-munkamenet-környezet) beállításához a PowerShell-munkamenetben a további ASR-műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="1b9aa-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b9aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1b9aa-104">SYNTAX</span></span>

```
Import-AzureRmRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b9aa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1b9aa-105">DESCRIPTION</span></span>
<span data-ttu-id="1b9aa-106">Az **import-AzureRmRecoveryServicesAsrVaultSettingsFile** parancsmag importálja az Azure-webhely helyreállítási Vault-beállításait tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="1b9aa-106">The **Import-AzureRmRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="1b9aa-107">A Vault-beállítások fájl az aktuális munkamenetben a következő Azure-webhely-helyreállítási műveletek boltozat-környezetének beállítására szolgál.</span><span class="sxs-lookup"><span data-stu-id="1b9aa-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="1b9aa-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1b9aa-108">EXAMPLES</span></span>

### <span data-ttu-id="1b9aa-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1b9aa-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzureRmRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="1b9aa-110">Importálja a megadott helyreállítási szolgáltatások Vault-beállítási fájlját, és az importált boltozat beállításait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="1b9aa-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="1b9aa-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1b9aa-111">PARAMETERS</span></span>

### <span data-ttu-id="1b9aa-112">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1b9aa-112">-Confirm</span></span>
<span data-ttu-id="1b9aa-113">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1b9aa-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b9aa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b9aa-114">-DefaultProfile</span></span>
<span data-ttu-id="1b9aa-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1b9aa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="1b9aa-116">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="1b9aa-116">-Path</span></span>
<span data-ttu-id="1b9aa-117">Az ASR-Vault beállítási fájl mappájának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b9aa-117">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="1b9aa-118">Ez a fájl letölthető a helyreállítási szolgáltatások Vault-portálról, és helyben tárolható.</span><span class="sxs-lookup"><span data-stu-id="1b9aa-118">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

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

### <span data-ttu-id="1b9aa-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b9aa-119">-WhatIf</span></span>
<span data-ttu-id="1b9aa-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1b9aa-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b9aa-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1b9aa-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b9aa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b9aa-122">CommonParameters</span></span>
<span data-ttu-id="1b9aa-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1b9aa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b9aa-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b9aa-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b9aa-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b9aa-125">INPUTS</span></span>

### <span data-ttu-id="1b9aa-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1b9aa-126">System.String</span></span>

## <span data-ttu-id="1b9aa-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b9aa-127">OUTPUTS</span></span>

### <span data-ttu-id="1b9aa-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="1b9aa-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="1b9aa-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1b9aa-129">NOTES</span></span>

## <span data-ttu-id="1b9aa-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1b9aa-130">RELATED LINKS</span></span>

[<span data-ttu-id="1b9aa-131">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="1b9aa-131">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesAsrVaultSettingsFile.md)
