---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
ms.openlocfilehash: 104bb05b4a01f5407c56e6c89de632a1ec5ab475
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927617"
---
# <span data-ttu-id="95c53-101">Update-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="95c53-101">Update-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="95c53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95c53-102">SYNOPSIS</span></span>
<span data-ttu-id="95c53-103">Frissíti az MSI-t a helyreállítási szolgáltatások tárolóján.</span><span class="sxs-lookup"><span data-stu-id="95c53-103">Updates MSI to the recovery services vault.</span></span>

## <span data-ttu-id="95c53-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="95c53-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesVault -ResourceGroupName <string> -Name <string> -IdentityType <MSIdentity>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95c53-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="95c53-105">DESCRIPTION</span></span>
<span data-ttu-id="95c53-106">Ezzel a parancsmagot használva lehet hozzáadni vagy eltávolítani az MSI-t a helyreállítási szolgáltatások tárolóból.</span><span class="sxs-lookup"><span data-stu-id="95c53-106">This cmdlet is used to add or remove  the MSI from the recovery services vault.</span></span> <span data-ttu-id="95c53-107">Az -IdentityType paraméter használatával SystemAssigned identitást rendelhet az RSVaulthoz.</span><span class="sxs-lookup"><span data-stu-id="95c53-107">Use -IdentityType param to assign a SystemAssigned identity to the RSVault.</span></span> <span data-ttu-id="95c53-108">A IdentityType None használatával távolítsa el az MSI-t a tárolóból.</span><span class="sxs-lookup"><span data-stu-id="95c53-108">Use IdentityType None to remove the MSI from the vault.</span></span>

## <span data-ttu-id="95c53-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="95c53-109">EXAMPLES</span></span>

### <span data-ttu-id="95c53-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="95c53-110">Example 1</span></span>
```powershell
PS C:\> Update-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName" -IdentityType SystemAssigned
```

<span data-ttu-id="95c53-111">Ezzel a parancsmaggal systemassigned identitást adhat a helyreállítási szolgáltatások tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="95c53-111">This cmdlet is used to add a SystemAssigned identity to a recovery services vault.</span></span>

## <span data-ttu-id="95c53-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95c53-112">PARAMETERS</span></span>

### <span data-ttu-id="95c53-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95c53-113">-DefaultProfile</span></span>
<span data-ttu-id="95c53-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="95c53-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95c53-115">-Name</span><span class="sxs-lookup"><span data-stu-id="95c53-115">-Name</span></span>

<span data-ttu-id="95c53-116">A frissítenie kell a helyreállítási szolgáltatások tárolóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="95c53-116">Specifies the name of the recovery services vault to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95c53-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95c53-117">-ResourceGroupName</span></span>

<span data-ttu-id="95c53-118">Annak az Azure-erőforráscsoportnak a neve, amelyben a helyreállítási szolgáltatások tárolója jelen van.</span><span class="sxs-lookup"><span data-stu-id="95c53-118">Specifies the name of the Azure resource group where recovery services vault is present.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95c53-119">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="95c53-119">-IdentityType</span></span>
<span data-ttu-id="95c53-120">A Helyreállítási szolgáltatások tárolóhoz rendelt MSI-típus.</span><span class="sxs-lookup"><span data-stu-id="95c53-120">The MSI type assigned to Recovery Services Vault.</span></span>

```yaml
Type: MSIdentity
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95c53-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95c53-121">-Confirm</span></span>
<span data-ttu-id="95c53-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="95c53-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95c53-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95c53-123">-WhatIf</span></span>
<span data-ttu-id="95c53-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="95c53-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95c53-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="95c53-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95c53-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95c53-126">CommonParameters</span></span>
<span data-ttu-id="95c53-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95c53-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95c53-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95c53-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95c53-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95c53-129">INPUTS</span></span>

### <span data-ttu-id="95c53-130">System.String</span><span class="sxs-lookup"><span data-stu-id="95c53-130">System.String</span></span>

## <span data-ttu-id="95c53-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="95c53-131">OUTPUTS</span></span>

### <span data-ttu-id="95c53-132">Microsoft.Azure.Management.RecoveryServices.Models.Vault</span><span class="sxs-lookup"><span data-stu-id="95c53-132">Microsoft.Azure.Management.RecoveryServices.Models.Vault</span></span>

## <span data-ttu-id="95c53-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="95c53-133">NOTES</span></span>

## <span data-ttu-id="95c53-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="95c53-134">RELATED LINKS</span></span>
