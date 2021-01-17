---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
ms.openlocfilehash: cdde8169c4b068b986910dc3bfc5de446833f5ff
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378291"
---
# <span data-ttu-id="17b49-101">Update-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="17b49-101">Update-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="17b49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17b49-102">SYNOPSIS</span></span>
<span data-ttu-id="17b49-103">Frissíti az MSI-t a helyreállítási szolgáltatások tárolóján.</span><span class="sxs-lookup"><span data-stu-id="17b49-103">Updates MSI to the recovery services vault.</span></span>

## <span data-ttu-id="17b49-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="17b49-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesVault -ResourceGroupName <string> -Name <string> -IdentityType <MSIdentity>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17b49-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="17b49-105">DESCRIPTION</span></span>
<span data-ttu-id="17b49-106">Ezzel a parancsmagot használva lehet hozzáadni vagy eltávolítani az MSI-t a helyreállítási szolgáltatások tárolóból.</span><span class="sxs-lookup"><span data-stu-id="17b49-106">This cmdlet is used to add or remove  the MSI from the recovery services vault.</span></span> <span data-ttu-id="17b49-107">Az -IdentityType paraméter használatával SystemAssigned identitást rendelhet az RSVaulthoz.</span><span class="sxs-lookup"><span data-stu-id="17b49-107">Use -IdentityType param to assign a SystemAssigned identity to the RSVault.</span></span> <span data-ttu-id="17b49-108">Az IdentityType None használatával távolítsa el az MSI-t a tárolóból.</span><span class="sxs-lookup"><span data-stu-id="17b49-108">Use IdentityType None to remove the MSI from the vault.</span></span>

## <span data-ttu-id="17b49-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="17b49-109">EXAMPLES</span></span>

### <span data-ttu-id="17b49-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="17b49-110">Example 1</span></span>
```powershell
PS C:\> Update-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName" -IdentityType SystemAssigned
```

<span data-ttu-id="17b49-111">Ezzel a parancsmaggal SystemAssigned identitást adhat hozzá a helyreállítási szolgáltatások tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="17b49-111">This cmdlet is used to add a SystemAssigned identity to a recovery services vault.</span></span>

## <span data-ttu-id="17b49-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17b49-112">PARAMETERS</span></span>

### <span data-ttu-id="17b49-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17b49-113">-DefaultProfile</span></span>
<span data-ttu-id="17b49-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="17b49-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17b49-115">-Name</span><span class="sxs-lookup"><span data-stu-id="17b49-115">-Name</span></span>

<span data-ttu-id="17b49-116">A frissítenie kell a helyreállítási szolgáltatások tárolóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="17b49-116">Specifies the name of the recovery services vault to update.</span></span>

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

### <span data-ttu-id="17b49-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17b49-117">-ResourceGroupName</span></span>

<span data-ttu-id="17b49-118">Annak az Azure-erőforráscsoportnak a neve, amelyben a helyreállítási szolgáltatások tárolója jelen van.</span><span class="sxs-lookup"><span data-stu-id="17b49-118">Specifies the name of the Azure resource group where recovery services vault is present.</span></span>

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

### <span data-ttu-id="17b49-119">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="17b49-119">-IdentityType</span></span>
<span data-ttu-id="17b49-120">A Helyreállítási szolgáltatások tárolóhoz rendelt MSI-típus.</span><span class="sxs-lookup"><span data-stu-id="17b49-120">The MSI type assigned to Recovery Services Vault.</span></span>

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

### <span data-ttu-id="17b49-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17b49-121">-Confirm</span></span>
<span data-ttu-id="17b49-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="17b49-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17b49-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17b49-123">-WhatIf</span></span>
<span data-ttu-id="17b49-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="17b49-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17b49-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="17b49-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17b49-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17b49-126">CommonParameters</span></span>
<span data-ttu-id="17b49-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17b49-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17b49-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17b49-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17b49-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17b49-129">INPUTS</span></span>

### <span data-ttu-id="17b49-130">System.String</span><span class="sxs-lookup"><span data-stu-id="17b49-130">System.String</span></span>

## <span data-ttu-id="17b49-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17b49-131">OUTPUTS</span></span>

### <span data-ttu-id="17b49-132">Microsoft.Azure.Management.RecoveryServices.Models.Vault</span><span class="sxs-lookup"><span data-stu-id="17b49-132">Microsoft.Azure.Management.RecoveryServices.Models.Vault</span></span>

## <span data-ttu-id="17b49-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="17b49-133">NOTES</span></span>

## <span data-ttu-id="17b49-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17b49-134">RELATED LINKS</span></span>
