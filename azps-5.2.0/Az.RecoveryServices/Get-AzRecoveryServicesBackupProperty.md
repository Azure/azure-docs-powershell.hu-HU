---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: efe463bab4195dfb09692f76d0e02e3aeaa59344
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356033"
---
# <span data-ttu-id="49380-101">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="49380-101">Get-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="49380-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49380-102">SYNOPSIS</span></span>
<span data-ttu-id="49380-103">Biztonsági mentési tulajdonságokat kap.</span><span class="sxs-lookup"><span data-stu-id="49380-103">Gets Backup properties.</span></span>

## <span data-ttu-id="49380-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="49380-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49380-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="49380-105">DESCRIPTION</span></span>
<span data-ttu-id="49380-106">A **Get-AzRecoveryServicesBackupProperty** parancsmag biztonsági mentési tulajdonságokat kap a Helyreállítási szolgáltatások tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="49380-106">The **Get-AzRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="49380-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="49380-107">EXAMPLES</span></span>

### <span data-ttu-id="49380-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="49380-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="49380-109">Szerezze be a biztonságimásolat-tároló tulajdonságát a tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="49380-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="49380-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49380-110">PARAMETERS</span></span>

### <span data-ttu-id="49380-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49380-111">-DefaultProfile</span></span>
<span data-ttu-id="49380-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="49380-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49380-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="49380-113">-Vault</span></span>
<span data-ttu-id="49380-114">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49380-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="49380-115">A tárolónak **AzureRmRecoveryServicesVault** objektumnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="49380-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49380-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49380-116">CommonParameters</span></span>
<span data-ttu-id="49380-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49380-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49380-118">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49380-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49380-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49380-119">INPUTS</span></span>

### <span data-ttu-id="49380-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="49380-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="49380-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49380-121">OUTPUTS</span></span>

### <span data-ttu-id="49380-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="49380-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="49380-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="49380-123">NOTES</span></span>

## <span data-ttu-id="49380-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49380-124">RELATED LINKS</span></span>
