---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
ms.openlocfilehash: dc73939aaae76c0444307cbd1aa6bfb08711b2e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837973"
---
# <span data-ttu-id="c3260-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="c3260-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="c3260-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c3260-102">SYNOPSIS</span></span>
<span data-ttu-id="c3260-103">Átlátszó adattitkosítási tanúsítvány hozzáadása az adott felügyelt példányhoz</span><span class="sxs-lookup"><span data-stu-id="c3260-103">Adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="c3260-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c3260-104">SYNTAX</span></span>

```
Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ManagedInstanceName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3260-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c3260-105">DESCRIPTION</span></span>
<span data-ttu-id="c3260-106">A Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate egy átlátszó adattitkosítási tanúsítványt ad hozzá az adott felügyelt példányhoz.</span><span class="sxs-lookup"><span data-stu-id="c3260-106">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="c3260-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c3260-107">EXAMPLES</span></span>

### <span data-ttu-id="c3260-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c3260-108">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ManagedInstanceName "YourManagedInstanceName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

## <span data-ttu-id="c3260-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c3260-109">PARAMETERS</span></span>

### <span data-ttu-id="c3260-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3260-110">-DefaultProfile</span></span>
<span data-ttu-id="c3260-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3260-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3260-112">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="c3260-112">-ManagedInstanceName</span></span>
<span data-ttu-id="c3260-113">A felügyelt példány neve</span><span class="sxs-lookup"><span data-stu-id="c3260-113">The managed instance name</span></span>

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

### <span data-ttu-id="c3260-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3260-114">-PassThru</span></span>
<span data-ttu-id="c3260-115">A sikeres végrehajtáskor a hozzáadott tanúsítványállapot-objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="c3260-115">On Successful execution, returns certificate object that was added.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3260-116">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="c3260-116">-Password</span></span>
<span data-ttu-id="c3260-117">Az átlátszó adattitkosítási tanúsítvány jelszava</span><span class="sxs-lookup"><span data-stu-id="c3260-117">The Password for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3260-118">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="c3260-118">-PrivateBlob</span></span>
<span data-ttu-id="c3260-119">A privát blob az átlátszó adattitkosítási tanúsítványhoz</span><span class="sxs-lookup"><span data-stu-id="c3260-119">The Private blob for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3260-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3260-120">-ResourceGroupName</span></span>
<span data-ttu-id="c3260-121">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c3260-121">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3260-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c3260-122">-Confirm</span></span>
<span data-ttu-id="c3260-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c3260-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3260-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3260-124">-WhatIf</span></span>
<span data-ttu-id="c3260-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c3260-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3260-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c3260-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3260-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3260-127">CommonParameters</span></span>
<span data-ttu-id="c3260-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c3260-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3260-129">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c3260-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3260-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3260-130">INPUTS</span></span>

### <span data-ttu-id="c3260-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="c3260-131">None</span></span>

## <span data-ttu-id="c3260-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3260-132">OUTPUTS</span></span>

### <span data-ttu-id="c3260-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c3260-133">System.Boolean</span></span>

## <span data-ttu-id="c3260-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c3260-134">NOTES</span></span>

## <span data-ttu-id="c3260-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3260-135">RELATED LINKS</span></span>
