---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 4e0b74ead08a3b944e66b46a6fee0fb71976b223
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929434"
---
# <span data-ttu-id="b4ed1-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="b4ed1-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="b4ed1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4ed1-102">SYNOPSIS</span></span>
<span data-ttu-id="b4ed1-103">Visszaadja egy helyreállítási szolgáltatás tároló tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="b4ed1-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="b4ed1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b4ed1-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4ed1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b4ed1-105">DESCRIPTION</span></span>
<span data-ttu-id="b4ed1-106">A **Get-AzRecoveryServicesVaultProperty** parancsmag visszaadja a helyreállítási szolgáltatások tároló tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="b4ed1-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="b4ed1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b4ed1-107">EXAMPLES</span></span>

### <span data-ttu-id="b4ed1-108">1. példa: A tároló tulajdonságainak lekérte</span><span class="sxs-lookup"><span data-stu-id="b4ed1-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
PS C:\> $encryption.encryptionProperties
```

<span data-ttu-id="b4ed1-109">Az első parancs egy tárolóobjektumot kap, majd a $vault tárolja.</span><span class="sxs-lookup"><span data-stu-id="b4ed1-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="b4ed1-110">A második parancs beveszi a tároló tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="b4ed1-110">The second command Gets the Vault Properties.</span></span> <span data-ttu-id="b4ed1-111">Ezután hozzáférhetünk a tároló titkosításiTulajdonságokhoz.</span><span class="sxs-lookup"><span data-stu-id="b4ed1-111">Next we access the encryptionProperties of the vault.</span></span>

## <span data-ttu-id="b4ed1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4ed1-112">PARAMETERS</span></span>

### <span data-ttu-id="b4ed1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4ed1-113">-DefaultProfile</span></span>
<span data-ttu-id="b4ed1-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4ed1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4ed1-115">-VaultId</span><span class="sxs-lookup"><span data-stu-id="b4ed1-115">-VaultId</span></span>
<span data-ttu-id="b4ed1-116">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b4ed1-116">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b4ed1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4ed1-117">CommonParameters</span></span>
<span data-ttu-id="b4ed1-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4ed1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4ed1-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4ed1-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4ed1-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4ed1-120">INPUTS</span></span>

### <span data-ttu-id="b4ed1-121">System.String</span><span class="sxs-lookup"><span data-stu-id="b4ed1-121">System.String</span></span>

## <span data-ttu-id="b4ed1-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4ed1-122">OUTPUTS</span></span>

### <span data-ttu-id="b4ed1-123">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="b4ed1-123">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="b4ed1-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b4ed1-124">NOTES</span></span>

## <span data-ttu-id="b4ed1-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4ed1-125">RELATED LINKS</span></span>

[<span data-ttu-id="b4ed1-126">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b4ed1-126">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="b4ed1-127">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="b4ed1-127">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
