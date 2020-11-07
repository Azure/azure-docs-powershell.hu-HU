---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/import-azrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: f630c8392ccfe68a399db80b7d55aef787fb48ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669679"
---
# <span data-ttu-id="46d4a-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="46d4a-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="46d4a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="46d4a-102">SYNOPSIS</span></span>
<span data-ttu-id="46d4a-103">Importálja a megadott ASR-tároló beállítási fájlját a boltozat környezetének (PowerShell-munkamenet-környezet) beállításához a PowerShell-munkamenetben a további ASR-műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="46d4a-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

## <span data-ttu-id="46d4a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="46d4a-104">SYNTAX</span></span>

```
Import-AzRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46d4a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="46d4a-105">DESCRIPTION</span></span>
<span data-ttu-id="46d4a-106">Az **import-AzRecoveryServicesAsrVaultSettingsFile** parancsmag importálja az Azure-webhely helyreállítási Vault-beállításait tartalmazó fájlt.</span><span class="sxs-lookup"><span data-stu-id="46d4a-106">The **Import-AzRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="46d4a-107">A Vault-beállítások fájl az aktuális munkamenetben a következő Azure-webhely-helyreállítási műveletek boltozat-környezetének beállítására szolgál.</span><span class="sxs-lookup"><span data-stu-id="46d4a-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="46d4a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="46d4a-108">EXAMPLES</span></span>

### <span data-ttu-id="46d4a-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="46d4a-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="46d4a-110">Importálja a megadott helyreállítási szolgáltatások Vault-beállítási fájlját, és az importált boltozat beállításait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="46d4a-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="46d4a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="46d4a-111">PARAMETERS</span></span>

### <span data-ttu-id="46d4a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46d4a-112">-DefaultProfile</span></span>
<span data-ttu-id="46d4a-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="46d4a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d4a-114">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="46d4a-114">-Path</span></span>
<span data-ttu-id="46d4a-115">Az ASR-Vault beállítási fájl mappájának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="46d4a-115">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="46d4a-116">Ez a fájl letölthető a helyreállítási szolgáltatások Vault-portálról, és helyben tárolható.</span><span class="sxs-lookup"><span data-stu-id="46d4a-116">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

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

### <span data-ttu-id="46d4a-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="46d4a-117">-Confirm</span></span>
<span data-ttu-id="46d4a-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="46d4a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46d4a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46d4a-119">-WhatIf</span></span>
<span data-ttu-id="46d4a-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="46d4a-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46d4a-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="46d4a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46d4a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d4a-122">CommonParameters</span></span>
<span data-ttu-id="46d4a-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="46d4a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d4a-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46d4a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d4a-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="46d4a-125">INPUTS</span></span>

### <span data-ttu-id="46d4a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="46d4a-126">System.String</span></span>

## <span data-ttu-id="46d4a-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46d4a-127">OUTPUTS</span></span>

### <span data-ttu-id="46d4a-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="46d4a-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="46d4a-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="46d4a-129">NOTES</span></span>

## <span data-ttu-id="46d4a-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46d4a-130">RELATED LINKS</span></span>

[<span data-ttu-id="46d4a-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="46d4a-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzRecoveryServicesAsrVaultSettingsFile.md)
