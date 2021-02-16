---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 48454b3b6bda283763b05657b0bc652fa9973233
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158523"
---
# <span data-ttu-id="ea09e-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="ea09e-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="ea09e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea09e-102">SYNOPSIS</span></span>

<span data-ttu-id="ea09e-103">A tároló környezetének beállítását.</span><span class="sxs-lookup"><span data-stu-id="ea09e-103">Sets vault context.</span></span>

## <span data-ttu-id="ea09e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ea09e-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea09e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ea09e-105">DESCRIPTION</span></span>

<span data-ttu-id="ea09e-106">A **Set-AzRecoveryServicesVaultContext parancsmag** beállítja a tároló környezetét az Azure Webhely-helyreállítási szolgáltatásokhoz.</span><span class="sxs-lookup"><span data-stu-id="ea09e-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="ea09e-107">Figyelmeztetés: Ezt a parancsmagot egy későbbi, törési változással kapcsolatos kiadásban elavultnak jük.</span><span class="sxs-lookup"><span data-stu-id="ea09e-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="ea09e-108">Ezt a helyére nem fogjuk cserélni.</span><span class="sxs-lookup"><span data-stu-id="ea09e-108">There will be no replacement for it.</span></span> <span data-ttu-id="ea09e-109">Kérjük, használja a -VaultId paramétert a helyreállítási szolgáltatások minden parancsában.</span><span class="sxs-lookup"><span data-stu-id="ea09e-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="ea09e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ea09e-110">EXAMPLES</span></span>

### <span data-ttu-id="ea09e-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="ea09e-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="ea09e-112">A tároló környezetének beállítását.</span><span class="sxs-lookup"><span data-stu-id="ea09e-112">Sets vault context.</span></span>

## <span data-ttu-id="ea09e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea09e-113">PARAMETERS</span></span>

### <span data-ttu-id="ea09e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea09e-114">-DefaultProfile</span></span>

<span data-ttu-id="ea09e-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ea09e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea09e-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="ea09e-116">-Vault</span></span>

<span data-ttu-id="ea09e-117">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ea09e-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="ea09e-118">A tárolónak **AzureRmRecoveryServicesVault** objektumnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="ea09e-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="ea09e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea09e-119">CommonParameters</span></span>
<span data-ttu-id="ea09e-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea09e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea09e-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea09e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea09e-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea09e-122">INPUTS</span></span>

### <span data-ttu-id="ea09e-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="ea09e-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="ea09e-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea09e-124">OUTPUTS</span></span>

### <span data-ttu-id="ea09e-125">System.Void</span><span class="sxs-lookup"><span data-stu-id="ea09e-125">System.Void</span></span>

## <span data-ttu-id="ea09e-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ea09e-126">NOTES</span></span>

## <span data-ttu-id="ea09e-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea09e-127">RELATED LINKS</span></span>
