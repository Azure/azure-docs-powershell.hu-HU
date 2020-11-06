---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
Module Name: Azure
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 922c7e7055c51990b28b472805a68563c94b3e6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505160"
---
# <span data-ttu-id="00333-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="00333-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="00333-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="00333-102">SYNOPSIS</span></span>
<span data-ttu-id="00333-103">Létrehoz egy konfigurációs objektumot az SQL Server Key Vault hitelesítő adatairól egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="00333-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00333-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="00333-104">SYNTAX</span></span>

```
New-AzureVMSqlServerKeyVaultCredentialConfig [-Enable] [[-CredentialName] <String>]
 [[-AzureKeyVaultUrl] <String>] [[-ServicePrincipalName] <String>] [[-ServicePrincipalSecret] <SecureString>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="00333-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="00333-105">DESCRIPTION</span></span>

## <span data-ttu-id="00333-106">Példák</span><span class="sxs-lookup"><span data-stu-id="00333-106">EXAMPLES</span></span>

## <span data-ttu-id="00333-107">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="00333-107">PARAMETERS</span></span>

### <span data-ttu-id="00333-108">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="00333-108">-Enable</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00333-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="00333-109">-CredentialName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00333-110">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="00333-110">-AzureKeyVaultUrl</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00333-111">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="00333-111">-ServicePrincipalName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00333-112">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="00333-112">-ServicePrincipalSecret</span></span>
```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00333-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="00333-113">-Profile</span></span>
<span data-ttu-id="00333-114">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="00333-114">@{Text=}</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Utilities.Common.AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00333-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="00333-115">-InformationAction</span></span>
<span data-ttu-id="00333-116">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="00333-116">@{Text=}</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00333-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="00333-117">-InformationVariable</span></span>
<span data-ttu-id="00333-118">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="00333-118">@{Text=}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00333-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00333-119">CommonParameters</span></span>
<span data-ttu-id="00333-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="00333-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00333-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00333-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00333-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="00333-122">INPUTS</span></span>

## <span data-ttu-id="00333-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00333-123">OUTPUTS</span></span>

## <span data-ttu-id="00333-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="00333-124">NOTES</span></span>

## <span data-ttu-id="00333-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00333-125">RELATED LINKS</span></span>

