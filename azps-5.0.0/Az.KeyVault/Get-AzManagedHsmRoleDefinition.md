---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsmroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleDefinition.md
ms.openlocfilehash: 60ba6fbf57fa9e1ac9e25a913fb9755902b56ddd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185307"
---
# <span data-ttu-id="6a149-101">Get-AzManagedHsmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="6a149-101">Get-AzManagedHsmRoleDefinition</span></span>

## <span data-ttu-id="6a149-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a149-102">SYNOPSIS</span></span>
<span data-ttu-id="6a149-103">A megadott felügyelt HSM listához tartozó szerepkör-definíciók.</span><span class="sxs-lookup"><span data-stu-id="6a149-103">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="6a149-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a149-104">SYNTAX</span></span>

### <span data-ttu-id="6a149-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6a149-105">Interactive (Default)</span></span>
```
Get-AzManagedHsmRoleDefinition [-HsmName] <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6a149-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6a149-106">ByName</span></span>
```
Get-AzManagedHsmRoleDefinition [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a149-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a149-107">DESCRIPTION</span></span>
<span data-ttu-id="6a149-108">A megadott felügyelt HSM listához tartozó szerepkör-definíciók.</span><span class="sxs-lookup"><span data-stu-id="6a149-108">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="6a149-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6a149-109">EXAMPLES</span></span>

### <span data-ttu-id="6a149-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6a149-110">Example 1</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleDefinition -HsmName myHsm -Scope "/keys"

RoleName                              Description Permissions
--------                              ----------- -----------
Managed HSM Administrator                         1 permission(s)
Managed HSM Crypto Officer                        1 permission(s)
Managed HSM Crypto User                           1 permission(s)
Managed HSM Policy Administrator                  1 permission(s)
Managed HSM Crypto Auditor                        1 permission(s)
Managed HSM Crypto Service Encryption             1 permission(s)
Managed HSM Backup                                1 permission(s)
```

<span data-ttu-id="6a149-111">A példa felsorolja az összes szerepkört a "/Keys" hatókörben.</span><span class="sxs-lookup"><span data-stu-id="6a149-111">The example lists all the roles at "/keys" scope.</span></span>

### <span data-ttu-id="6a149-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="6a149-112">Example 2</span></span>
```powershell
PS C:\> $backupRole = Get-AzManagedHsmRoleDefinition -HsmName myHsm -RoleDefinitionName "managed hsm backup"

PS C:\> $backupRole.Permissions

AllowedActions DeniedActions AllowedDataActions DeniedDataActions
-------------- ------------- ------------------ -----------------
0 action(s)    0 action(s)   3 action(s)        0 action(s)

PS C:\> $backupRole.Permissions.AllowedDataActions

Microsoft.KeyVault/managedHsm/backup/start/action
Microsoft.KeyVault/managedHsm/backup/status/action
Microsoft.KeyVault/managedHsm/keys/backup/action

RoleName                              Description Permissions
--------                              ----------- -----------
Managed HSM Administrator                         1 permission(s)
Managed HSM Crypto Officer                        1 permission(s)
Managed HSM Crypto User                           1 permission(s)
Managed HSM Policy Administrator                  1 permission(s)
Managed HSM Crypto Auditor                        1 permission(s)
Managed HSM Crypto Service Encryption             1 permission(s)
Managed HSM Backup                                1 permission(s)
```

<span data-ttu-id="6a149-113">A példa a "felügyelt HSM biztonsági másolat" szerepkört kapja, és megvizsgálja az engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="6a149-113">The example gets the "Managed HSM Backup" role and inspects its permissions.</span></span>

## <span data-ttu-id="6a149-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a149-114">PARAMETERS</span></span>

### <span data-ttu-id="6a149-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a149-115">-DefaultProfile</span></span>
<span data-ttu-id="6a149-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a149-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a149-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="6a149-117">-HsmName</span></span>
<span data-ttu-id="6a149-118">A HSM neve.</span><span class="sxs-lookup"><span data-stu-id="6a149-118">Name of the HSM.</span></span>

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

### <span data-ttu-id="6a149-119">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="6a149-119">-RoleDefinitionName</span></span>
<span data-ttu-id="6a149-120">A beolvasott szerepkör definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="6a149-120">Name of the role definition to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: RoleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a149-121">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="6a149-121">-Scope</span></span>
<span data-ttu-id="6a149-122">Az a hatókör, amelyen a szerepkör-hozzárendelés vagy-definíció érvényes, például "/" vagy "/Keys" vagy "/keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="6a149-122">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="6a149-123">a "/" érték kihagyása esetén használatos.</span><span class="sxs-lookup"><span data-stu-id="6a149-123">'/' is used when omitted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a149-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a149-124">CommonParameters</span></span>
<span data-ttu-id="6a149-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a149-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a149-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6a149-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a149-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a149-127">INPUTS</span></span>

### <span data-ttu-id="6a149-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="6a149-128">None</span></span>

## <span data-ttu-id="6a149-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a149-129">OUTPUTS</span></span>

### <span data-ttu-id="6a149-130">Microsoft. Azure. Command. PSKeyVaultRoleDefinition. models.</span><span class="sxs-lookup"><span data-stu-id="6a149-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="6a149-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a149-131">NOTES</span></span>

## <span data-ttu-id="6a149-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a149-132">RELATED LINKS</span></span>
