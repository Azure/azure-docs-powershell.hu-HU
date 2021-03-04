---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/import-azrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: b287e69093ca748d02cd3f630e3b38fb51cdf8f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007670"
---
# <span data-ttu-id="add62-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="add62-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="add62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="add62-102">SYNOPSIS</span></span>
<span data-ttu-id="add62-103">Importálja a megadott ASR tárolóbeállítási fájlt a tároló környezetének (PowerShell-munkamenetkörnyezet) beállítására a PowerShell-munkamenet későbbi ASR-műveleteihez.</span><span class="sxs-lookup"><span data-stu-id="add62-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

## <span data-ttu-id="add62-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="add62-104">SYNTAX</span></span>

```
Import-AzRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="add62-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="add62-105">DESCRIPTION</span></span>
<span data-ttu-id="add62-106">Az **Import-AzRecoveryServicesAsrVaultSettingsFile** parancsmag importálja az Azure Site Recovery tároló beállításfájlját.</span><span class="sxs-lookup"><span data-stu-id="add62-106">The **Import-AzRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="add62-107">A tárolóbeállításokat tárolófájl az aktuális munkamenet későbbi Azure-webhely-helyreállítási műveleteinek tárolókörnyezetének beállítására szolgál.</span><span class="sxs-lookup"><span data-stu-id="add62-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="add62-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="add62-108">EXAMPLES</span></span>

### <span data-ttu-id="add62-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="add62-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="add62-110">Importálja a helyreállítási szolgáltatások megadott tárolóbeállítás-fájlját, és visszaadja az importált tároló beállításait.</span><span class="sxs-lookup"><span data-stu-id="add62-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="add62-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="add62-111">PARAMETERS</span></span>

### <span data-ttu-id="add62-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="add62-112">-DefaultProfile</span></span>
<span data-ttu-id="add62-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="add62-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="add62-114">-Path</span><span class="sxs-lookup"><span data-stu-id="add62-114">-Path</span></span>
<span data-ttu-id="add62-115">Az ASR-tároló beállításait tartalmazó fájl mappa elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="add62-115">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="add62-116">Ez a fájl letölthető a Helyreállítási szolgáltatások tároló portálról, és helyben tárolható.</span><span class="sxs-lookup"><span data-stu-id="add62-116">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

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

### <span data-ttu-id="add62-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="add62-117">-Confirm</span></span>
<span data-ttu-id="add62-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="add62-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="add62-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="add62-119">-WhatIf</span></span>
<span data-ttu-id="add62-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="add62-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="add62-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="add62-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="add62-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="add62-122">CommonParameters</span></span>
<span data-ttu-id="add62-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="add62-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="add62-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="add62-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="add62-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="add62-125">INPUTS</span></span>

### <span data-ttu-id="add62-126">System.String</span><span class="sxs-lookup"><span data-stu-id="add62-126">System.String</span></span>

## <span data-ttu-id="add62-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="add62-127">OUTPUTS</span></span>

### <span data-ttu-id="add62-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="add62-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="add62-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="add62-129">NOTES</span></span>

## <span data-ttu-id="add62-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="add62-130">RELATED LINKS</span></span>

[<span data-ttu-id="add62-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="add62-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzRecoveryServicesAsrVaultSettingsFile.md)
