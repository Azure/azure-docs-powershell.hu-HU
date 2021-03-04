---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 04fa3c9a7024b8a9e1f525a4ef131ae151f25804
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942242"
---
# <span data-ttu-id="3553f-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="3553f-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="3553f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3553f-102">SYNOPSIS</span></span>

<span data-ttu-id="3553f-103">A tároló környezetének beállítását.</span><span class="sxs-lookup"><span data-stu-id="3553f-103">Sets vault context.</span></span>

## <span data-ttu-id="3553f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3553f-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3553f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3553f-105">DESCRIPTION</span></span>

<span data-ttu-id="3553f-106">A **Set-AzRecoveryServicesVaultContext parancsmag** beállítja a tároló környezetét az Azure Webhely-helyreállítási szolgáltatásokhoz.</span><span class="sxs-lookup"><span data-stu-id="3553f-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="3553f-107">Figyelmeztetés: Ezt a parancsmagot egy későbbi, törési változással kapcsolatos kiadásban elavultnak jük.</span><span class="sxs-lookup"><span data-stu-id="3553f-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="3553f-108">Erre a helyére nem lesz szükség.</span><span class="sxs-lookup"><span data-stu-id="3553f-108">There will be no replacement for it.</span></span> <span data-ttu-id="3553f-109">Kérjük, használja a -VaultId paramétert a helyreállítási szolgáltatások minden parancsában.</span><span class="sxs-lookup"><span data-stu-id="3553f-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="3553f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3553f-110">EXAMPLES</span></span>

### <span data-ttu-id="3553f-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="3553f-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="3553f-112">A tároló környezetének beállítását.</span><span class="sxs-lookup"><span data-stu-id="3553f-112">Sets vault context.</span></span>

## <span data-ttu-id="3553f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3553f-113">PARAMETERS</span></span>

### <span data-ttu-id="3553f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3553f-114">-DefaultProfile</span></span>

<span data-ttu-id="3553f-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3553f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3553f-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="3553f-116">-Vault</span></span>

<span data-ttu-id="3553f-117">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3553f-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="3553f-118">A tárolónak **AzureRmRecoveryServicesVault** objektumnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="3553f-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="3553f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3553f-119">CommonParameters</span></span>
<span data-ttu-id="3553f-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3553f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3553f-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3553f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3553f-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3553f-122">INPUTS</span></span>

### <span data-ttu-id="3553f-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="3553f-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="3553f-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3553f-124">OUTPUTS</span></span>

### <span data-ttu-id="3553f-125">System.Void</span><span class="sxs-lookup"><span data-stu-id="3553f-125">System.Void</span></span>

## <span data-ttu-id="3553f-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3553f-126">NOTES</span></span>

## <span data-ttu-id="3553f-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3553f-127">RELATED LINKS</span></span>
