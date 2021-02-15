---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: da541e9f019dfb82efc496ce60ab300229e36ac0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160155"
---
# <span data-ttu-id="a5a9c-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="a5a9c-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="a5a9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5a9c-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a9c-103">Visszaadja egy helyreállítási szolgáltatás tároló tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="a5a9c-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="a5a9c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a5a9c-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5a9c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a5a9c-105">DESCRIPTION</span></span>
<span data-ttu-id="a5a9c-106">A **Get-AzRecoveryServicesVaultProperty** parancsmag visszaadja a helyreállítási szolgáltatások tároló tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="a5a9c-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="a5a9c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a5a9c-107">EXAMPLES</span></span>

### <span data-ttu-id="a5a9c-108">1. példa: A tároló tulajdonságainak lekérte</span><span class="sxs-lookup"><span data-stu-id="a5a9c-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
PS C:\> $encryption.encryptionProperties
```

<span data-ttu-id="a5a9c-109">Az első parancs egy tárolóobjektumot kap, majd a $vault tárolja.</span><span class="sxs-lookup"><span data-stu-id="a5a9c-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="a5a9c-110">A második parancs beveszi a tároló tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="a5a9c-110">The second command Gets the Vault Properties.</span></span> <span data-ttu-id="a5a9c-111">Ezután hozzáférhetünk a tároló titkosításiTulajdonságokhoz.</span><span class="sxs-lookup"><span data-stu-id="a5a9c-111">Next we access the encryptionProperties of the vault.</span></span>

## <span data-ttu-id="a5a9c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5a9c-112">PARAMETERS</span></span>

### <span data-ttu-id="a5a9c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a9c-113">-DefaultProfile</span></span>
<span data-ttu-id="a5a9c-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5a9c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5a9c-115">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a5a9c-115">-VaultId</span></span>
<span data-ttu-id="a5a9c-116">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a5a9c-116">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5a9c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a9c-117">CommonParameters</span></span>
<span data-ttu-id="a5a9c-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5a9c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a9c-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5a9c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a9c-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5a9c-120">INPUTS</span></span>

### <span data-ttu-id="a5a9c-121">System.String</span><span class="sxs-lookup"><span data-stu-id="a5a9c-121">System.String</span></span>

## <span data-ttu-id="a5a9c-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5a9c-122">OUTPUTS</span></span>

### <span data-ttu-id="a5a9c-123">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="a5a9c-123">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="a5a9c-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a5a9c-124">NOTES</span></span>

## <span data-ttu-id="a5a9c-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5a9c-125">RELATED LINKS</span></span>

[<span data-ttu-id="a5a9c-126">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a5a9c-126">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="a5a9c-127">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="a5a9c-127">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
