---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 48454b3b6bda283763b05657b0bc652fa9973233
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479222"
---
# <span data-ttu-id="8fa9b-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="8fa9b-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="8fa9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fa9b-102">SYNOPSIS</span></span>

<span data-ttu-id="8fa9b-103">A tároló környezetének beállítását.</span><span class="sxs-lookup"><span data-stu-id="8fa9b-103">Sets vault context.</span></span>

## <span data-ttu-id="8fa9b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8fa9b-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8fa9b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8fa9b-105">DESCRIPTION</span></span>

<span data-ttu-id="8fa9b-106">A **Set-AzRecoveryServicesVaultContext parancsmag** beállítja a tároló környezetét az Azure Webhely-helyreállítási szolgáltatásokhoz.</span><span class="sxs-lookup"><span data-stu-id="8fa9b-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="8fa9b-107">Figyelmeztetés: Ezt a parancsmagot egy későbbi, törési változással kapcsolatos kiadásban elavultnak jük.</span><span class="sxs-lookup"><span data-stu-id="8fa9b-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="8fa9b-108">Erre a helyére nem lesz szükség.</span><span class="sxs-lookup"><span data-stu-id="8fa9b-108">There will be no replacement for it.</span></span> <span data-ttu-id="8fa9b-109">Kérjük, használja a -VaultId paramétert a helyreállítási szolgáltatások minden parancsában.</span><span class="sxs-lookup"><span data-stu-id="8fa9b-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="8fa9b-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8fa9b-110">EXAMPLES</span></span>

### <span data-ttu-id="8fa9b-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="8fa9b-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="8fa9b-112">A tároló környezetének beállítását.</span><span class="sxs-lookup"><span data-stu-id="8fa9b-112">Sets vault context.</span></span>

## <span data-ttu-id="8fa9b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8fa9b-113">PARAMETERS</span></span>

### <span data-ttu-id="8fa9b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fa9b-114">-DefaultProfile</span></span>

<span data-ttu-id="8fa9b-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8fa9b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fa9b-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="8fa9b-116">-Vault</span></span>

<span data-ttu-id="8fa9b-117">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8fa9b-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="8fa9b-118">A tárolónak **AzureRmRecoveryServicesVault** objektumnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="8fa9b-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="8fa9b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fa9b-119">CommonParameters</span></span>
<span data-ttu-id="8fa9b-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fa9b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fa9b-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8fa9b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fa9b-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8fa9b-122">INPUTS</span></span>

### <span data-ttu-id="8fa9b-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="8fa9b-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="8fa9b-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fa9b-124">OUTPUTS</span></span>

### <span data-ttu-id="8fa9b-125">System.Void</span><span class="sxs-lookup"><span data-stu-id="8fa9b-125">System.Void</span></span>

## <span data-ttu-id="8fa9b-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8fa9b-126">NOTES</span></span>

## <span data-ttu-id="8fa9b-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8fa9b-127">RELATED LINKS</span></span>
