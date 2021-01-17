---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/import-azrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: de3604a4bf1f9c46bf88b2f3cda25982672e9096
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378376"
---
# <span data-ttu-id="e8973-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="e8973-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="e8973-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8973-102">SYNOPSIS</span></span>
<span data-ttu-id="e8973-103">A megadott ASR tárolóbeállítási fájl importálva adja meg a tároló környezetét (PowerShell-munkamenet környezetét) a PowerShell-munkamenet későbbi ASR-műveleteihez.</span><span class="sxs-lookup"><span data-stu-id="e8973-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

## <span data-ttu-id="e8973-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e8973-104">SYNTAX</span></span>

```
Import-AzRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8973-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e8973-105">DESCRIPTION</span></span>
<span data-ttu-id="e8973-106">Az **Import-AzRecoveryServicesAsrVaultSettingsFile** parancsmag importálja az Azure Site Recovery tároló beállításfájlját.</span><span class="sxs-lookup"><span data-stu-id="e8973-106">The **Import-AzRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="e8973-107">A tárolóbeállításokat tárolófájl az aktuális munkamenet későbbi Azure-webhely-helyreállítási műveleteinek tárolókörnyezetének beállítására szolgál.</span><span class="sxs-lookup"><span data-stu-id="e8973-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="e8973-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e8973-108">EXAMPLES</span></span>

### <span data-ttu-id="e8973-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="e8973-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="e8973-110">Importálja a helyreállítási szolgáltatások megadott tárolóbeállítás-fájlját, és visszaadja az importált tároló beállításait.</span><span class="sxs-lookup"><span data-stu-id="e8973-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="e8973-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8973-111">PARAMETERS</span></span>

### <span data-ttu-id="e8973-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8973-112">-DefaultProfile</span></span>
<span data-ttu-id="e8973-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e8973-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e8973-114">-Path</span><span class="sxs-lookup"><span data-stu-id="e8973-114">-Path</span></span>
<span data-ttu-id="e8973-115">Az ASR-tároló beállításait tartalmazó fájl mappa elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e8973-115">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="e8973-116">Ez a fájl letölthető a Helyreállítási szolgáltatások tároló portálról, és helyben tárolható.</span><span class="sxs-lookup"><span data-stu-id="e8973-116">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

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

### <span data-ttu-id="e8973-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8973-117">-Confirm</span></span>
<span data-ttu-id="e8973-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e8973-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8973-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8973-119">-WhatIf</span></span>
<span data-ttu-id="e8973-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e8973-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8973-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e8973-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8973-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8973-122">CommonParameters</span></span>
<span data-ttu-id="e8973-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8973-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8973-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8973-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8973-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e8973-125">INPUTS</span></span>

### <span data-ttu-id="e8973-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e8973-126">System.String</span></span>

## <span data-ttu-id="e8973-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8973-127">OUTPUTS</span></span>

### <span data-ttu-id="e8973-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="e8973-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="e8973-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e8973-129">NOTES</span></span>

## <span data-ttu-id="e8973-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8973-130">RELATED LINKS</span></span>

[<span data-ttu-id="e8973-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="e8973-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzRecoveryServicesAsrVaultSettingsFile.md)
