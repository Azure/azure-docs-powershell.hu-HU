---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 6602f1005877d4e38546338fd44d8fc51991a7b6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195194"
---
# <span data-ttu-id="302ad-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="302ad-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="302ad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="302ad-102">SYNOPSIS</span></span>
<span data-ttu-id="302ad-103">A helyreállítási szolgáltatások boltozatának tulajdonságait számítja ki.</span><span class="sxs-lookup"><span data-stu-id="302ad-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="302ad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="302ad-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="302ad-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="302ad-105">DESCRIPTION</span></span>
<span data-ttu-id="302ad-106">A **Get-AzRecoveryServicesVaultProperty** parancsmag a helyreállítási szolgáltatások boltozatának tulajdonságait számítja ki.</span><span class="sxs-lookup"><span data-stu-id="302ad-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="302ad-107">Példák</span><span class="sxs-lookup"><span data-stu-id="302ad-107">EXAMPLES</span></span>

### <span data-ttu-id="302ad-108">Példa 1: a boltozat tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="302ad-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
```

<span data-ttu-id="302ad-109">Az első parancs a boltozat objektumot kapja, majd a $vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="302ad-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="302ad-110">A második parancs a boltozat tulajdonságait kapja.</span><span class="sxs-lookup"><span data-stu-id="302ad-110">The second command Gets the Vault Properties.</span></span>

## <span data-ttu-id="302ad-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="302ad-111">PARAMETERS</span></span>

### <span data-ttu-id="302ad-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="302ad-112">-DefaultProfile</span></span>
<span data-ttu-id="302ad-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="302ad-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="302ad-114">-VaultId</span><span class="sxs-lookup"><span data-stu-id="302ad-114">-VaultId</span></span>
<span data-ttu-id="302ad-115">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="302ad-115">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="302ad-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="302ad-116">CommonParameters</span></span>
<span data-ttu-id="302ad-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="302ad-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="302ad-118">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="302ad-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="302ad-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="302ad-119">INPUTS</span></span>

### <span data-ttu-id="302ad-120">System. String</span><span class="sxs-lookup"><span data-stu-id="302ad-120">System.String</span></span>

## <span data-ttu-id="302ad-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="302ad-121">OUTPUTS</span></span>

### <span data-ttu-id="302ad-122">Microsoft. Azure. Management. RecoveryServices. backup. models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="302ad-122">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="302ad-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="302ad-123">NOTES</span></span>

## <span data-ttu-id="302ad-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="302ad-124">RELATED LINKS</span></span>

[<span data-ttu-id="302ad-125">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="302ad-125">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="302ad-126">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="302ad-126">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
